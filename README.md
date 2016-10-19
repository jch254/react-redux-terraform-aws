# React-redux-terraform-aws

A simple React/Redux-powered UI to front a simple [Serverless web API](https://github.com/jch254/serverless-es6-dynamodb-webapi). Written with a functional mindset - this project uses Immutable.js and Reselect for efficient client-side data manipulation.

This project is deployed to AWS on S3, CloudFront is used as a CDN and Route 53 is used for DNS. All infrastructure is defined as code in the [/infrastructure](../master/infrastructure) directory. Manual steps suck so this project uses Bitbucket Pipelines to automate the build and deployment to AWS - see [bitbucket-pipelines.yml](../master/bitbucket-pipelines.yml). AWS credentials are set in this file to take advantage of [Bitbucket Pipelines environment variables](https://confluence.atlassian.com/bitbucket/environment-variables-in-bitbucket-pipelines-794502608.html).

### Main technologies used

* [React](https://facebook.github.io/react/)
* [Redux](https://github.com/reactjs/redux/)
* [Redux-saga](https://github.com/yelouafi/redux-saga/)
* [Immutable.js](https://github.com/facebook/immutable-js/)
* [Reselect](https://github.com/jxnblk/rebass)
* [Webpack](https://github.com/webpack/webpack)
* [Node.js](https://github.com/nodejs/node)

--

**API_BASE_URI environment variable must be set before `npm run` commands below.**

E.g. `API_BASE_URI="https://serverless-web-api.amazon.com" npm run dev`

### Running locally (with live re-loading)

1. Run the following commands in the app's root directory then open http://localhost:3001

```
npm install
npm run dev
```

### Building the production version
1. Run the following commands in the app's root directory then check the /dist folder

```
npm install
npm run build
```

### Deployment/Infrastructure

Refer to the [/infrastructure](../master/infrastructure) directory.
