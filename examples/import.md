# How to import and export databases

To test all examples, first you need to import a database to your local environment.

## Importing from a dump directory

Go to [datasets](../datasets) directory and choose a database. In this example I will be using **movies_dump**:

```bash
$ mongorestore movies_dump
```

Extremely simple, right? Be sure that MongoDB process is running and you are using this command inside [datasets](../datasets) directory.

## Exporting a database to a dump directory

Like the example above, export your MongoDB data is pretty simple too. Just use:

```bash
$ mongodump -d my_database_dump
```
... where **my_database_dump** is the name you want for your dump directory.
