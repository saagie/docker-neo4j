# Neo4j

Docker image base on offical Neo4j image.

The only difference is the path of mounted volume where to store data: `/data-neo4j` instead of `/data`.

## Run it

`docker run -d --rm --name neo4j -p7474:7474 -p7687:7687 -v $(pwd)/data-neo4j:/data-neo4j saagie/docker-neo4j`

