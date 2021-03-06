Example Alexa with NodeJS Lambda SECURE REST 
============================================

This example project shows how to build an Alexa skill, and allow the skill to use a NodeJS Lambda function. The supporting lambda function allows the Alexa skill to call a secure REST service endpoint. The REST service endpoint is the Marvel developer API. 

Therefore, you will need to sign-up for your own developer account to get a public and private access token. The private and public keys can be added to the appropriate MARVEL_PUBLIC_KEY and MARVEL_PRIVATE_KEY constant values.  The Lambda function also needss to have the api key assigned to you from the Alexa skills setup.

### Building a NodeJS project from a blank starting point
Create a NodeJS project from scratch using the `npm init` command. Fill in the information on the prompt
```
npm init
```
Next add the alexa-sdk to the project and dependency.
```
npm install --save alexa-sdk
```
You can test the lambda function on your local environment without having to deploy up to Amazon lambda by using the lightweight aws-lambda-local library. Install this as follows:
```
npm install -g aws-lambda-local
```

Alternatively you can create a package.json and add the necessary dependencies above. Then type in the following in the directory where package.json is located.
```
npm install
```
### Alexa skills
To integrate an Alexa skill to this Lambda function you will need to go to the [AWS Developer console](https://developer.amazon.com/) and create an Alexa Skills Kit.

### Authors
* **Brij R**


Either case these two commands simulates an alexa skills call to the AWS Lambda function. The environment file is called testEvent.json.

### Deploy to AWS Lambda
Once you have built and tested your lambda function locally you can deploy it to AWS lambda. Go to [AWS Console](https://console.aws.amazon.com). Go to the AWS Lambda service to create a function. The alexa skills package dependencies and core NodeJS packages are already in a basic template in AWS Lambda. All you really need to do is copy the `index.js` file into the AWS Lambda Code editor. 


### References

* [AWS NodeJS SDK](https://github.com/alexa/alexa-skills-kit-sdk-for-nodejs) - AWS NodeJs sdk
* [Lambda-local](https://github.com/ashiina/lambda-local) - AWS lightweight serverless local lambda testing
