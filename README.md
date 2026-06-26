# db2-scripts
General repo for db2-specific scripts

These scripts can be called through external tools such as TOAD for DB2/Datapoint, dBeaver, etc with the assumption you'd manually export the result set and pass it through to db2cli, where it can be excuted via <code>db2 -tvf <sqlstmt.sql></code>. 

I anticipate having a cleaner solution where db2cli just outputs to .sql file vs manual workaround as I've done it before to make things easier for my teammates.

<!--
Alternatively, you can execute internally with the following steps:

[code]'db2 -tvf gen_runstats_code.sql > runstats.sql' && sed -s '/ //g' [/code]
and run 
-->
