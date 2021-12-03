I did it with a pain)

I made simple code in mysql with 3 tables called:

-workers:
    -id  int (primaty key);
    -name varchar;
    -surname varchar;
    -position varchar;

-organisation:
    -id int (primary key);
    -name varchar;
    -occupation varchar;

-tasks:
    -id int (primary key);
    -description varchar;
    -worker_id (FOREIGN KEY from workers(id));
    -organisation_id (FOREIGN KEY from organisation(id));


Made backups and one dump. Did I have problems? - Uuuuugh yeah)

Imported data from my local mysql into RDS.


Then I have made dynamodb with a simple view.