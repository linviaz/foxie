# Partially import Oracle database

The following substracts from the TAGS project report on 28th March 2018.

> Dependent on the export tool used for the exported dump files, imp or data pump impdp can be used for importing dump files. 
> The reason for importing partially of the whole GSI database is because the limit of the ORACLE Database 11g Express Edition is 4G, where the full GSI Oracle database is 10.7G.
> The procedure for importing the BOREHOLE,CONTACT,LOCATION,GEOTECH,LOOKUP schemas are as following:

+ create new Users with Grant/Admin/Default (testing) rights under SYSTEM/Other Users as BOREHOLE,CONTACT,LOCATION,GEOTECH.LOOKUP with their corresponding passwords.
+ Create new Connections named BOREHOLE,CONTACT,LOCATION,GEOTECH,LOOKUP under the BOREHOLE,CONTACT,LOCATION,GEOTECH,LOOKUP users.
+ Create new DBAs named BOREHOLE,CONTACT,LOCATION,GEOTECH,LOOKUP under the responding connections.
+ After configuring the database, import the schemas from the dump file using:

```
imp SYSTEM/PASSWORD FROMUSER=BOREHOLE,CONTACT,LOACTION,GEOTECH,LOOKUP TOUSER=BOREHOLE,CONTACT,LOCATION,GEOTECH,LOOKUP log = import.log
```

# DQL
 - column names of table:
 ```
 SELECT * FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_NAME = 'table_name';
 ```
 
 


