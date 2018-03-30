# Neo4j

Docker image base on offical Neo4j image.

The only difference is the path of mounted volume where to store data: `/data-neo4j` instead of `/data`.

## Run it

`docker run -d --rm --name neo4j -p7474:7474 -p7687:7687 -v $(pwd)/data-neo4j:/data-neo4j saagie/docker-neo4j`

### Customizing ports

If you want to run Neo4j web interface on another port (default is 7474), you can use either `NEO4J_dbms_connector_http_listen__address` or `PORT0` environment variable.
If you want to customize Bolt port, use `NEO4J_dbms_connector_bolt_listen__address` or `PORT1`

Example:
`docker run -d --rm --name neo4j -p1234:1234 -p9876:9876 --env PORT0=1234 --env PORT1=9876 -v $(pwd)/data-neo4j:/data-neo4j saagie/docker-neo4j`
