# Autonomous Database for Developers

Repository providing various demos using an Oracle Autonomous Database. Each demo is a Maven module depending upon the `common` module. 

## Setup
You'll need to set several environment variables to be able to run these examples:
- region: the OCI region where the Autonomous Database has been provisioned
- user: the username you want to connect to the Autonomous Database 
  (this will be the username that you'll create during **Demo 1** and use later on)
- password: the password to connect to the Autonomous Database
- database: the database name you want to connect to (unique name, see your tnsnames.ora inside the wallet)

#### Example
- `export region=eu-marseille-1` (see [here for a list](https://docs.cloud.oracle.com/en-us/iaas/Content/General/Concepts/regions.htm#top))
- `export user=bob`
- `export password=5uper_Pa55w0rd` set this as the same as the ADMIN user (see [here for password complexity 
  requirements](https://docs.oracle.com/en/cloud/paas/autonomous-database/adbsa/manage-users-create.html#GUID-72DFAF2A-C4C3-4FAC-A75B-846CC6EDBA3F))
- `export database=iq1ffzid3wfss2e_myatps`

## Demos
The following demos are presented in a logical order so it is preferable starting with demo 1, then demo 2, etc...   
- [Demo 1 - Using the REST Enabled SQL Service to create a new database user](./sqlviarest)
- [Demo 2 - Connecting using Spring Boot JDBC](./connecting)
- [Demo 3 - Calling PL/SQL functions to manage database User Locks](./userlocks)

### Coming next...
- Demo 4 - Generating AWR and ADDM reports in order to analyze performance
- Demo 5 -  Distinguishing the service names to use, what and when?
- Demo 6 - Enabling Automatic Index reporting
