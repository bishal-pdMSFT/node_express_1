# Steps to deploy a Node express app to AWS Elastic Beanstalk Service:

1. Create an Elastic Beanstalk application
2. Create a "web server" Environment to be used in the application and set the base configuration to "Node.Js" platform
3. Create S3 bucket to store the source code zip file
4. Create an IAM user with permissions:AWSElasticBeanstalkFullAccess 
5. Use the Security credentials of the IAM user and set the following Secrets in GitHub Repo
   <ul>
    <li>AWS_ACCESS_KEY_ID</li>
    <li>AWS_SECRET_ACCESS_KEY </li>
    <li>AWS_DEFAULT_REGION</li>
</ul>
 
6. In the workflow yaml:
    <ul>
    <li>Checkout and Zip the contents</li>
    <li>Copy the zip to s3 bucket </li>
    <li>Create the app for ElasticBeanstalk</li>
    <li>Deploy the app for ElasticBeanstalk</li>
</ul>
