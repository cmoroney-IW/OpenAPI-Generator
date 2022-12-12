## Prerequisites

- Follow documentation on https://maven.apache.org/install.html and install Maven
- Follow documentation on https://nodejs.org/en/download/ and install node.js
- Once node.js is installed, install OpenAPI Generator in the command line by entering `npm install @openapitools/openapi-generator-cli -g` in a terminal

## Installation

- Copy `CurrentAccount.yaml` from this repository into a local directory
- Open a terminal in the same directory as `CurrentAccount.yaml` and run `openapi-generator-cli generate -i OpenApi.yaml -g spring -o .` - this will generate the application from the OpenAPI specification within `CurrentAccount.yaml`
- After the code has been generated,

- Run `mvn clean spring-boot:run` in your terminal - this will run the application
