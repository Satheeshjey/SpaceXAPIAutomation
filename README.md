# SpaceX_APIAutomation


## Pre Requisites 

Install newman CLI using following command.

    npm install -g newman

Install newman reporting libraries

    npm install -g newman-reporter-htmlextra


## Execution

    Collection : SpaceX.postman_collection.json

    Env File : env.json

Open the command prompt and execute the following command by passing environment variables in a file.

## Using environment json file to pass parameters.
    > newman run SpaceX.postman_collection.json -e env.json

## Passing parameters via CLI
    > newman run SpaceX.postman_collection.json --env-var "httpProtocol=https" --env-var "hostName=api.spacexdata.com" --env-var "version=v4"

## Generating report using htmlExtra
    > newman run SpaceX.postman_collection.json -e env.json -r htmlextra

## Viewing the report
When using option "-r htmlextra", it will create a folder called newman in the working dir and generate a html report.


