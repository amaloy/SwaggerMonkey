# SwaggerMonkey
Provides service load by making random calls based on a Swagger JSON file.

These environment variables must be defined:

* `SM_SWAGGER_FILE`, may be a local file or http/s URL
* `SM_TARGET_HOST`, comma-separated list of hosts
* `SM_TARGET_PORT`

Optional environment variables:

* `SM_SCHEME` example: `SM_SCHEME=http`, if you don't want to use the scheme defined in swagger
* `SM_INCLUDE_PATH`, example: `SM_INCLUDE_PATH=/myresource/myid`, comma-separated list of paths to add to query that aren't automatically selected
* `SM_ID_FIELDS`, example: `SM_ID_FIELDS=id,uuid`, default is just `id`, used for detecting possible ids to query

Direct execution:

`SM_SWAGGER_FILE=http://192.168.1.2/swagger.json SM_TARGET_HOST=192.168.1.2 SM_TARGET_PORT=8080 ./swaggermonkey`

Docker:

`docker build -t swaggermonkey .`

`docker run -e SM_SWAGGER_FILE=http://192.168.200.2/swagger.json -e SM_TARGET_HOST=192.168.200.2 -e SM_TARGET_PORT=8080 swaggermonkey`
