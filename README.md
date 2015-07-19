# BettawayTest
Coding test for Bettaway Logistics Programmer Analyst Position
by Heather Propes


Install
1. Set up a MySQL db called bettaway
2. Import the file at src/main/webapp/resources/sql/createUsers.sql to create a users table
3. In weblogic, create datasource 
	*Name it “jdbc/bettaway” and the jndi name must also be “jdbc/bettaway”.
	*Domain Structure (left panel) -> mydomain -> Services -> Data Sources
	*Fill out the details that pertain to your configuration
	*Make sure that you check “myserver” in targets tab to deploy to proper domain 
4. In weblogic, deploy BettawayWebapp-1.0-SNAPSHOT.war as a web application (I’m guessing you know how to do this).
5. Verify that web application and datasource are both showing “OK” in weblogic console.
6. Now go to http://localhost:7001/BettawayWebapp/ and try the Bettaway At-Home Test Web Application.


To-Do
1. System runs out of memory after about 10 builds. Is this because of my badly underpowered VM, or a memory leak? Use Weblogic to diagnose. 
2. Figure out how best to use JPA to regenerate tables upon deployment, automatically, or with a homemade script, as in this article: http://www.hildeberto.com/2009/05/table-generation-strategy-revised.html.
3. Why is maven not picking up src/main/resources on “build with dependencies”? Debug and resolve.
4. List.xhtml contains all functionality. Remove unused .xmtml files:  Edit.xhtml, View.xhtml, Create.xhtml.
5. After a record is deleted, it shows in the “create” form. Fix this.
6. Fix status messages so they are more grammatically correct.
7. Make UI Components a little bigger and more user-friendly.

