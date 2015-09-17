SchemaCrawler Docker Image
==========================

A Docker image for the [SchemaCrawler](http://sualeh.github.io/SchemaCrawler/) command line tool.  The image contains the full SchemaCrawler package in `/schemacrawler`.


## Sample usage

Assuming some_db is a container with postgres listening on the default port.  Update the rest of the flags as appropriate.

```
$ docker run -v $(pwd):/output --link some_db:db --rm symfoni/schemabuilder:14.03.01 -server=postgresql -host=db -user=postgres -password=password -database=database -infolevel=maximum -command=graph --outputfile=/output/database.png
```

