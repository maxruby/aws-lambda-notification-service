# Serverless Lambda Notification Service

## Description
A simple Notification service consisting of a serverless lambda function that sends emails in unordered queue using the AWS SQS and SES, based on the [Serverless framework Bootcamp](https://www.udemy.com/course/serverless-framework/).

## Dependencies
* [serverless-pseudo-parameters plugin](https://www.npmjs.com/package/serverless-pseudo-parameters): Support for CloudFormation Pseudo Parameters.
* [serverless-bundle plugin](https://www.npmjs.com/package/serverless-pseudo-parameters): Webpack plugin providing zero configuration for bundling JavaScript including modern ES6/ES7 features.

## Setup
Created using [codingly.io](https://github.com/codingly-io/sls-base) as follows:

```shell
$ sls create --name notification-service --template-url https://github.com/codingly-io/sls-base
$ cd notification-service
$ npm install
```

## Development
Trigger manually sending an e-mail via the SQS which disptaches the SES handler lambda function sendMail:

```shell
$ sls invoke -f notification-service -l
```

## Deployment
```shell
$ sls deploy -v
```