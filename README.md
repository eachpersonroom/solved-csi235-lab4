Download Link: https://assignmentchef.com/product/solved-csi235-lab4
<br>
<h2>Task 1  Automatic recording of information in a database</h2>

In this task we implemented the first part of a system that verifies the following access control rule.

<em>An item can be added to an order only by a user who created the order. </em>

If you skipped the <strong>Prologue </strong>section of specification <strong>Laboratory 4</strong> then it is recommended to read it now.

Implement SQL script solution1.sql that performs the following actions.

<ul>

 <li>First, the script creates a relational table to store information about a new order key and a name of user who created a new order.</li>

 <li>Next, the script creates a database trigger, that automatically inserts into a relational table created in the previous step, a key of a new order and a name of a user who created the order. If an order is deleted then the trigger must automatically delete information about an order key and a user who earlier created the order. A type of a trigger is up to you.</li>

 <li>Next, the script comprehensively tests the trigger. A test must include listing of the contents of a table with order keys and user names, insertion of an order, listing of the contents of the table again, deletion of an order, and listing of the contents of the table again.</li>

</ul>

When ready, process SQL script solution1.sql and create a report from processing of the script in a file solution1.lst.

Your report must include a listing of all PL/SQL statements processed. To achieve that put the following SQLcl commands:

SPOOL solution1

SET ECHO ON

SET FEEDBACK ON

SET LINESIZE 200

SET PAGESIZE 400

SET SERVEROUTPUT ON




at the beginning of SQL script and




SPOOL OFF




at the end of SQL script.




<h2>Deliverables</h2>

A file solution1.lst with a report from the implementation of a script solution1.sql that creates a new relational table, a database trigger, and tests the trigger.  A report must have no errors and it must list all SQL statements processed.

<u>                                                                                                                                                </u>

<h2>Task 2  Implementation of an access control rule</h2>

Task 1 must be implemented before Task 2.

In this task we implement the second part of a system that verifies the following access control rule.

<em>An item can be added to an order only by a user who created the order. </em>

If you skipped the <strong>Prologue </strong>section of specification <strong>Laboratory 4</strong> then it is recommended to read it now.

Implement SQL script solution2.sql that performs the following actions.




<ul>

 <li>First, the script creates a database trigger that fires whenever a new item is added to an order. The trigger must verify if a user who creates a new item is the same user who created an order into which a new item is added.</li>

</ul>




If a user who attempts to insert a new item into an order created by another user the trigger must abort the transaction and must display an error message.  Otherwise, the trigger does nothing.




<ul>

 <li>Next, the script tests the trigger.</li>

</ul>




A test must include creation of two new orders.




Then, insertion of a new item into one of the orders created a moment ago must be successful.




Next, the script updates one of the user names in a relational table created in Task 1.




Next, insertion of another item into an order created by a user whose name has been updated fails the access control rule.




Finally, insertion of an item to an order whose creator is unknown must also fail the access control rule.




In this task a processing error is a good news and we abolish a principle saying that no marks are granted for processing errors. Note, that it applies only to Task 2.




When ready, process SQL script solution2.sql and save a report from processing in a file solution2.lst.




Your report must include a listing of all PL/SQL statements processed. To achieve that put the following SQLcl commands:




SPOOL solution2

SET ECHO ON

SET FEEDBACK ON

SET LINESIZE 100

SET PAGESIZE 200

SET SERVEROUTPUT ON




at the beginning of SQL script and




SPOOL OFF




at the end of SQL script.




<h2>Deliverables</h2>

A file solution2.lst with a report from processing of SQL script solution2.sql. A report must list all SQL statements processed and all error messages.

<u>                                                                                                                                                </u>





