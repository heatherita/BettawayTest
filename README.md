# BettawayTest
Coding test for Bettaway Logistics Programmer Analyst Position
by Heather Propes


**Install Application**

Set up a MySQL db called bettaway.

Import the file at src/main/webapp/resources/sql/createUsers.sql to create a users table.

In weblogic console, create datasource in Domain Structure (left panel) -> mydomain -> Services -> Data Sources.
1) Name it “jdbc/bettaway” and the jndi name must also be “jdbc/bettaway”.
2) Fill out the details that pertain to your configuration.
3) Make sure that you check “myserver” (or whatever your server name is) in targets tab to deploy to proper domain. 

In weblogic, deploy BettawayWebapp-1.0-SNAPSHOT.war as a web application (I’m guessing you know how to do this).

Verify that web application and datasource are both showing “OK” in weblogic console.

Now go to http://localhost:7001/BettawayWebapp/ in a browser and try Heather Propes's Bettaway At-Home Test Web Application.

Contact Heather if anything breaks or if you have questions.


**Using Application**

Create - Simply fill in first name, last name, and DOB and click "save".

View - View all rows in table. Click "Next 10" to see additional.

Update - Click any field in "view" table and edit value. Click the check mark to save to database or the "x" to cancel.

Delete - Click the "destroy" link corresponding to a table row to delete the row.


**To-Do**

System runs out of memory after about 10 builds. Is this because of my badly underpowered VM, or a memory leak? Use Weblogic to diagnose. 

Figure out how best to use JPA to regenerate tables upon deployment, automatically, or with a homemade script, as in this article: http://www.hildeberto.com/2009/05/table-generation-strategy-revised.html.

Why is maven not picking up src/main/resources on “build with dependencies”? Debug and resolve.

List.xhtml contains all functionality. Remove unused .xmtml files:  Edit.xhtml, View.xhtml, Create.xhtml.

After a record is deleted, it shows in the “create” form. Fix this.

Fix status messages so they are more grammatically correct.

Make UI Components a little bigger and more user-friendly. Use buttons instead of links for controls.

