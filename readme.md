# Azure Web Apps Node.js Todo Sample

Quick demo on how to run a Node.js App on Azure

## Important pieces

### web.config

This file contains the info to tell us which file to start (in this case, `bin/www`)

### .deployment

This file tells us which file contains the deployment commands

### deploy.cmd

This file will run npm install for us when we deploy to the Azure Web App

## Set up on Azure

1. Fork this repo
2. Create a Web App
3. Add DB connection info as App Settings
    - PGUSER
    - PGPASSWORD
    - PGDATABASE
    - PGSERVER
4. Set up GitHub deployment
    1. Click on Deployment Options
    2. Choose GitHub
    3. Select the forked repo
    4. Click on Deployment Options again and wait for it to complete
5. Visit home page

## Develop and run locally

1. Clone this repo
2. Set up env variables
    - PGUSER
    - PGPASSWORD
    - PGDATABASE
    - PGSERVER
3. Run `npm install`
4. Run `npm start`

If you want to modify the server code, you'll need to run `npm run build` from the root directory

If you want to modify the client library, you'll need to navigate to the client directory and run `npm run build`

# Step-by-step procedure to setup CI/CD for your application

Below are the steps to setup CI/CD for your application on Azure:

1. Locally test your application code
2. Push it to a GitHub repo
3. Create azure resources in https://portal.azure.com or using az-cli commands
4. Sign-up for GitHubAction beta [here](https://github.com/features/actions)
5. Add a workflow file in your repo, using [templates](https://github.com/azure/actions-workflow-samples) or write your own custom workflow, containnig checkout, build and deploy steps.
6. Don't forget to configure triggers on your workflow.


## LICENSE

[MIT](LICENSE)
