## Descripción
#### Description

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 52495 -U postgres pico`Password is `postgres`
## Pistas 
What does a SQL database contain?
## Solución
utilizamos comandos de postgrest sql  para encontrar la flag
┌──(kali㉿kali)-[~/Desktop]
└─$ psql -h saturn.picoctf.net -p 52495 -U postgres pico
Password for user postgres: 
psql (16.1 (Debian 16.1-1+b1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# ls
pico-# 
pico-# 
pico-# 
pico-# SELECT * FROM mi_tabla;
ERROR:  syntax error at or near "ls"
LINE 1: ls
        ^
pico=# SELECT * FROM mi_tabla;
ERROR:  relation "mi_tabla" does not exist
LINE 1: SELECT * FROM mi_tabla;
                      ^
pico=# SELECT * FROM          
pico-# 
pico-# DW
pico-# 
pico-# DWA
pico-# AWDCLEAR
pico-# LIST
pico-# list
pico-# dwad
pico-# help
Use \? for help or press control-C to clear the input buffer.
pico-# \help
Available help:
  ABORT                            ALTER SYSTEM                     CREATE FOREIGN DATA WRAPPER      CREATE USER MAPPING              DROP ROUTINE                     NOTIFY
  ALTER AGGREGATE                  ALTER TABLE                      CREATE FOREIGN TABLE             CREATE VIEW                      DROP RULE                        PREPARE
  ALTER COLLATION                  ALTER TABLESPACE                 CREATE FUNCTION                  DEALLOCATE                       DROP SCHEMA                      PREPARE TRANSACTION
  ALTER CONVERSION                 ALTER TEXT SEARCH CONFIGURATION  CREATE GROUP                     DECLARE                          DROP SEQUENCE                    REASSIGN OWNED
  ALTER DATABASE                   ALTER TEXT SEARCH DICTIONARY     CREATE INDEX                     DELETE                           DROP SERVER                      REFRESH MATERIALIZED VIEW
  ALTER DEFAULT PRIVILEGES         ALTER TEXT SEARCH PARSER         CREATE LANGUAGE                  DISCARD                          DROP STATISTICS                  REINDEX
  ALTER DOMAIN                     ALTER TEXT SEARCH TEMPLATE       CREATE MATERIALIZED VIEW         DO                               DROP SUBSCRIPTION                RELEASE SAVEPOINT
  ALTER EVENT TRIGGER              ALTER TRIGGER                    CREATE OPERATOR                  DROP ACCESS METHOD               DROP TABLE                       RESET
  ALTER EXTENSION                  ALTER TYPE                       CREATE OPERATOR CLASS            DROP AGGREGATE                   DROP TABLESPACE                  REVOKE
  ALTER FOREIGN DATA WRAPPER       ALTER USER                       CREATE OPERATOR FAMILY           DROP CAST                        DROP TEXT SEARCH CONFIGURATION   ROLLBACK
  ALTER FOREIGN TABLE              ALTER USER MAPPING               CREATE POLICY                    DROP COLLATION                   DROP TEXT SEARCH DICTIONARY      ROLLBACK PREPARED
  ALTER FUNCTION                   ALTER VIEW                       CREATE PROCEDURE                 DROP CONVERSION                  DROP TEXT SEARCH PARSER          ROLLBACK TO SAVEPOINT
  ALTER GROUP                      ANALYZE                          CREATE PUBLICATION               DROP DATABASE                    DROP TEXT SEARCH TEMPLATE        SAVEPOINT
  ALTER INDEX                      BEGIN                            CREATE ROLE                      DROP DOMAIN                      DROP TRANSFORM                   SECURITY LABEL
  ALTER LANGUAGE                   CALL                             CREATE RULE                      DROP EVENT TRIGGER               DROP TRIGGER                     SELECT
  ALTER LARGE OBJECT               CHECKPOINT                       CREATE SCHEMA                    DROP EXTENSION                   DROP TYPE                        SELECT INTO
  ALTER MATERIALIZED VIEW          CLOSE                            CREATE SEQUENCE                  DROP FOREIGN DATA WRAPPER        DROP USER                        SET
  ALTER OPERATOR                   CLUSTER                          CREATE SERVER                    DROP FOREIGN TABLE               DROP USER MAPPING                SET CONSTRAINTS
  ALTER OPERATOR CLASS             COMMENT                          CREATE STATISTICS                DROP FUNCTION                    DROP VIEW                        SET ROLE
  ALTER OPERATOR FAMILY            COMMIT                           CREATE SUBSCRIPTION              DROP GROUP                       END                              SET SESSION AUTHORIZATION
  ALTER POLICY                     COMMIT PREPARED                  CREATE TABLE                     DROP INDEX                       EXECUTE                          SET TRANSACTION
  ALTER PROCEDURE                  COPY                             CREATE TABLE AS                  DROP LANGUAGE                    EXPLAIN                          SHOW
  ALTER PUBLICATION                CREATE ACCESS METHOD             CREATE TABLESPACE                DROP MATERIALIZED VIEW           FETCH                            START TRANSACTION
  ALTER ROLE                       CREATE AGGREGATE                 CREATE TEXT SEARCH CONFIGURATION DROP OPERATOR                    GRANT                            TABLE
  ALTER ROUTINE                    CREATE CAST                      CREATE TEXT SEARCH DICTIONARY    DROP OPERATOR CLASS              IMPORT FOREIGN SCHEMA            TRUNCATE
  ALTER RULE                       CREATE COLLATION                 CREATE TEXT SEARCH PARSER        DROP OPERATOR FAMILY             INSERT                           UNLISTEN
  ALTER SCHEMA                     CREATE CONVERSION                CREATE TEXT SEARCH TEMPLATE      DROP OWNED                       LISTEN                           UPDATE
  ALTER SEQUENCE                   CREATE DATABASE                  CREATE TRANSFORM                 DROP POLICY                      LOAD                             VACUUM
  ALTER SERVER                     CREATE DOMAIN                    CREATE TRIGGER                   DROP PROCEDURE                   LOCK                             VALUES
  ALTER STATISTICS                 CREATE EVENT TRIGGER             CREATE TYPE                      DROP PUBLICATION                 MERGE                            WITH
  ALTER SUBSCRIPTION               CREATE EXTENSION                 CREATE USER                      DROP ROLE                        MOVE                             
pico-# SELECT * FROM pg_database;
ERROR:  syntax error at or near "AWDCLEAR"
LINE 5: AWDCLEAR
        ^
pico=# \1
invalid command \1
Try \? for help.
pico=# \l
                                                      List of databases
   Name    |  Owner   | Encoding | Locale Provider |  Collate   |   Ctype    | ICU Locale | ICU Rules |   Access privileges   
-----------+----------+----------+-----------------+------------+------------+------------+-----------+-----------------------
 pico      | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |            |           | 
 postgres  | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |            |           | 
 template0 | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |            |           | =c/postgres          +
           |          |          |                 |            |            |            |           | postgres=CTc/postgres
 template1 | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |            |           | =c/postgres          +
           |          |          |                 |            |            |            |           | postgres=CTc/postgres
(4 rows)

pico=# \c pico
psql (16.1 (Debian 16.1-1+b1), server 15.2 (Debian 15.2-1.pgdg110+1))
You are now connected to database "pico" as user "postgres".
pico=# SELECT * FROM pico
pico-# \c pico
psql (16.1 (Debian 16.1-1+b1), server 15.2 (Debian 15.2-1.pgdg110+1))
You are now connected to database "pico" as user "postgres".
pico-# \c pico
psql (16.1 (Debian 16.1-1+b1), server 15.2 (Debian 15.2-1.pgdg110+1))
You are now connected to database "pico" as user "postgres".
pico-# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico-# select * from flags;
ERROR:  syntax error at or near "select"
LINE 2: select * from flags;
        ^
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 

## Bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}