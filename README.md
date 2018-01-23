# SwaggerMonkey
Provides service load by making random calls based on a Swagger JSON file.

These environment variables must be defined:

* `SM_SWAGGER_FILE`
* `SM_TARGET_HOST`
* `SM_TARGET_PORT`

Direct execution:

`SM_SWAGGER_FILE=http://192.168.1.2/swagger.json SM_TARGET_HOST=192.168.1.2 SM_TARGET_PORT=8080 ./swaggermonkey`

Docker:

`docker build -t swaggermonkey .`

`docker run -e SM_SWAGGER_FILE=http://192.168.200.2/swagger.json -e SM_TARGET_HOST=192.168.200.2 -e SM_TARGET_PORT=8080 swaggermonkey`
