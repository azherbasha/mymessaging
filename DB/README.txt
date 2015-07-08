Referance URL : http://www.postgresql.org/docs/8.1/static/backup.html
Note:Use compressed dumps. You can use your favorite compression program, for example gzip.

Backup:
-------
pg_dump dbname | gzip > filename.gz


Restore:
--------
gunzip -c filename.gz | psql dbname


Example:
=======
Backup:
-------
pg_dump dev_cb_messaging | gzip > ./dev-cb-messaging-backup.gz
Note:
----- 
1) Create one new direcotory from Outside of your project
2) Goto that directory and take the path name.
3) Switch User to Postgres and go to the directory path which you have created in step-1
4) Run the above command
5) Makesure that directory has got chmod 777 permissions
6) Then move the downloaded gz file to your project directory

Restore:
--------
gunzip -c dev-cb-messaging-backup.gz | psql dev_cb_messaging
Note:
-----
1) Goto DB directory and take the path name.
2) Switch User to Postgres and go to the directory path which you have created in step-1
4) Run the above command
