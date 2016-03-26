<h3>A minimal implementation of a RestExpress server</h3>

This sample is based on a RestExpress template project available as a maven archetype <a href='https://github.com/RestExpress/RestExpress-Archetype'>here</a><br/>

RestExpress is a compact Java framework that allows to quickly build scalable, containerless, RESTful microservices. See <a href='https://github.com/RestExpress/RestExpress'>here</a> for more informations about RestExpress<br/>

This sample makes a few changes to the template in order to see some concrete illustrations on the minimalist template (no need here for the databse integration...the archetype's github site provides two additional archetype for mongo-db and cassandra integration)

The project can be run just like the template

To run the project via Maven:

	mvn clean package exec:java

To create a 'fat' runnable jar file:

	mvn clean package

To run the jar file created via package

	java -jar target/{project-name}.jar [environment]


Configuration
-------------

By default, the 'mvn package' goal will create a fat jar file including the configuration files in src/main/resources.
These are loaded from the classpath at runtime. However, to override the values embedded in the jar file, simply create
a new configuration file on the classpath for the desired environment. For example, './config/dev/environment.properties'
and any settings in that file will get added to, or override settings embedded in the jar file. <br/>

Once the server is up and running....
-------------------------------------

The server will be listening (by default) on port 8081 on localhost. A few routes has been changed as shown in the code snippet below [extracted from the Routes.java class]

<pre>
	public static void define(Configuration config, RestExpress server)
    	{
		//TODO: Your routes here...
		//server.uri("/your/route/here/{sampleId}.{format}", config.getSampleController())
		server.uri("/simple/test/books/id1.xml", config.getSampleController())
			.method(HttpMethod.GET, HttpMethod.PUT, HttpMethod.DELETE)
			.name(Constants.Routes.SINGLE_SAMPLE);

		server.uri("/simple/test/books.xml", config.getSampleController())
			.action("readAll", HttpMethod.GET)
			.method(HttpMethod.POST)
			.name(Constants.Routes.SAMPLE_COLLECTION);
		// or...
		//		server.regex("/some.regex", config.getRouteController());
    	}
</pre>

The SampleController.java read method was also changed to return a "Hello world" message. We can invoke the server with an Http GET request such as <b><u>http://localhost:8081/simple/test/books/id1.xml</u></b><br/>
The response is shown below<br/><br/>
<img src='https://github.com/alainlompo/frontline-frontend/blob/master/restexpress/restexpress-minimal/src/main/resources/sample_request_003.png' alt='sample get response' />
