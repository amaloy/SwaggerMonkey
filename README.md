# SwaggerMonkey
Provides service load by making random calls based on a Swagger JSON file.

These environment variables must be defined:

* `SM_SWAGGER_FILE`
* `SM_TARGET_HOST`
* `SM_TARGET_PORT`

Example command:

`SM_SWAGGER_FILE=http://192.168.1.2/swagger.json SM_TARGET_HOST=192.168.1.2 SM_TARGET_PORT=8080 ./swaggermonkey`
