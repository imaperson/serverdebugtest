# Simple test servlet

Add the server to the Community Server Connector from disk at /usr/local/tomcat

Build a war file with ./mvnw package

Add a deployment from target/webapp-1.0.0-SNAPSHOT.war

Right click the tomcat server in the Community Server Connector and click `Edit Server`.  Add `"mapProperty.launch.env": {"TEST_ENV": "SUCCESS"},` to the json.

Start the server and go to http://localhost:8080/webapp-1.0.0-SNAPSHOT/test

Expected response is `Test env: 'SUCCESS'`

Stop the server.

Debug the server.  Hit escape when it askes for a project name.  Go to http://localhost:8080/webapp-1.0.0-SNAPSHOT/test

Response is now `Test env: 'null'`
