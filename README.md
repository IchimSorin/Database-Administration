# Database-Administration
Database Administration – Project Requirements

============================== Part 1 – The Physical Schema ==============================
1. Chose a database application that is of interest for you. It must use Oracle as the database
server. You should have minimum 5-6 tables.

2. Implement a script for tablespace creation. The tablespaces should be specific for your
application.
Pay attention to:

   The CREATE TABLESPACE command.

   Use different folders to simulate data distribution on different disks. For example
/ora/disk1, /ora/disk2.

3. Implement a script for objects creation. 
Be careful with:

   The application schema. The database objects should be included in a separate schema
(not sys/system) so the script should include the command for schema creation with
appropriate privileges

   The properties used at the segment level, so that their allocation matches the
tablespaces previously created. Also, the segment attributes should cover as much as
possible the physical schema.

   The segment types (there might be more than just tables and indexes)


============================== Part 2 – Performance Tuning ==============================
1. Implement a script for inserting data into the tables. At least one table should have hundreds of
thousands of rows (>100000) (you can use PL/SQL logic to do it).

2. Prepare at least 3 queries that need optimization: one query
with weak selectivity, one with good selectivity and one with joins. You should provide a
description of the purpose of each query (from a business perspective). Then you must obtain
the execution plan of each query and interpret it. Then you will apply optimization techniques to
make the queries more efficient.
Pay attention to:

   The optimization criteria (number of logical reads, execution time)

   Optimization technique (indexes, restructuring of the SQL query)


============================== Part 3 – Security and Audit ==============================
1. Implement the security component of the application at the database level. Identify for your
application the main user types, the privileges they need (write/read on specific tables), etc. For 
each category create an Oracle role and grant the necessary privileges. Create at least one user
for each category and grant the specific Oracle role. Then build a scenario (read/write data) that
proves that the privileges work for each role.

2. Choose one user of the application and implement an audit strategy for him. Specify what you
want to audit, why and the solution. Prove that the solution works by writing a test scenario.


============================== Part 4 – Backup & Recovery ==============================
1. Design a backup and recovery strategy for the database. The strategy must contain RPO and
RTO requirements and a description of the way these requirements are met.
2. Create a script that does the backup and then imagine a "crash" scenario with the necessary
steps required for recovering the data, based on your backup strategy.
