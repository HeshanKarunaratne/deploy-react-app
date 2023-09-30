# Getting Started with Create React App

### Steps
1. Generate a ReactApp using npx create-react-app {app_name}
2. Run the app using `npm run start`
3. Build the app using `npm run build`
4. Download AWSCLI for your machine
5. Setup credentials using `aws configure`
6. Add below scripts
~~~json
{
    "deploy-s3": "aws s3 --profile <profile-name> sync ./build/ s3://<bucket-name> --region us-east-1",
    "cache-bust": "aws --profile <profile-name> cloudfront create-invalidation --distribution-id <distribution-id> --paths \"/*\"",
}
~~~
7. Create an Invalidation in Cloudfront distribution
8. Make sure to add your `<profile-name>`, `<distribution-id>` and `<bucket-name>`