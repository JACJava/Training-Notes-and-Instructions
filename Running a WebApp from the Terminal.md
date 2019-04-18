## Running a WebApp from the Terminal

1.  Open a terminal
   
2.  Navigate to the root directory (i.e. c:\Users\Julie\Documents\GitHub\Java-BookstoreShoppingCart

3.  mvn clean install tomcat7:run

Once that is running the terminal should display something similar to the following:

INFO: Starting Servlet Engine: Apache Tomcat/7.0.47
May 21, 2018 10:22:35 PM org.apache.coyote.AbstractProtocol start
INFO: Starting ProtocolHandler ["http-bio-8080"]

4. Leave that running, and in another terminal type the following:

mvn -Pintegration verify

5.  In order to see your changes in a browser, make sure Tomcat is still running in your terminal, 
and visit http://localhost:8080/books/list in a browser to see the app running.