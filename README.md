# python-web-bottle-api-cockroachdb-single-node-without-ssl-raw-sql-simple

## Description
Simple web app that serves an api
for a bottle project.

Uses sqlalchemy query a table `dog` using raw sql.

Remotely tested with *testify*.

## Tech stack
- python
  - bottle
  - sqlalchemy
  - testify
  - response
- cockroachdb

## Docker stack
- python:latest
- cockroachdb/cockroach:v19.2.4

## To run
`sudo ./install.sh -u`
- Get all dogs: http://localhost/dog
  - Schema id, name, and color
- CRUD opperations
  - Create: curl -i -X PUT localhost/dog/<id>
  - Read: http://localhost/dog/<id>
  - Update: curl -i -X POST localhost/dog/<id>/<name>/<color>
  - Delete: curl -i -X DELETE localhost/dog/<id>

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
[Bottle sqlalchemy setup](https://github.com/iurisilvio/bottle-sqlalchemy/blob/master/examples/basic.py)
