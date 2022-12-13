# OpenAPI Code Generation

## Prerequisites

- Apache Maven installed: https://maven.apache.org/install.html for documentation
- Postman installed: https://www.postman.com/downloads/ for documentation
- Node.js installed: https://nodejs.org/en/download/ for documentation
- OpenAPI Generator CLI installed: Run `npm install @openapitools/openapi-generator-cli -g` in a terminal with node.js capacity to install

## Code Generation

- Clone or fork this repository into a local directory
- Open a terminal in the same directory as `CurrentAccount.yaml` and run `openapi-generator-cli generate -i CurrentAccount.yaml -g spring -o .` to generate the application from the OpenAPI specification within `CurrentAccount.yaml`

## Bug Fixing

- After the code has been generated, there is a bug that you must fix before being able to run the application
- Open `EnumConverterConfiguration.java` within `src/main/java/org/openapitools/configuration`
- Refactor `partyinvolvementtypevalues` and `partytypevalues` to begin with a capital letter, correctly import the dependencies, and finally delete the incorrect dependencies
- If done correctly, there should no longer be any linting errors with the application

## Testing

- Run `mvn clean spring-boot:run` in your terminal to run the application
- Open `localhost:8080` in your browser, which will redirect you to the Swagger interface documenting the endpoints within this API
- Open Postman and use the collection JSON file in the directory to test two GET endpoints of the API: **GET current account information** and **GET current account lien information**
