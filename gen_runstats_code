-- SQL that will dynamically create RUNSTATS commands for tables that meet desired criteria
-- Adjust accordingly for your own purposes and TEST in NON-PROD systems first.
-- 
-- Below statement pulls all tables with stats older than 30 days from db SAMPLE in DB2ADM instance owner schema
-- 
select ('RUNSTATS ON TABLE '
          || trim(TABSCHEMA)
          || '.'
          || trim(TABNAME)
          || ' WITH DISTRIBUTION ON KEY COLUMNS AND SAMPLED DETAILED INDEXES ALL;') as SQLSTMT
             from SYSCAT.TABLES
                  where TYPE='T'
                    and TABSCHEMA='DB2ADM'
                    and STATS_TIME < (current_timestamp - 30 days);
