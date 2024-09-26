# Project-Deploy a Static Website on AWS S3 with Terraform

This project showcases the deployment of a static website on AWS, utilizing S3 for storage and CloudFront for content delivery. Infrastructure is managed and automated using Terraform, with S3 handling state management and DynamoDB ensuring state locking.

## Features:

**S3:** Stores and hosts the static files for the website.

**CloudFront:** Delivers content globally, ensuring low-latency access.

**Terraform:** Implements infrastructure as code to automate the entire deployment process.

**Remote State Management:** Manages Terraform state in S3 with state locking provided by DynamoDB.


## Prerequisites: 
Before getting started with this project, make sure you have the following:

**An AWS account** with the necessary permissions to create S3 buckets, CloudFront distributions, and DynamoDB tables.

**Terraform** installed (version 1.0.0 or higher).

**AWS CLI** set up and configured with your credentials on your local machine.

## Infrastructure Setup
**S3 Bucket:**
Create an S3 bucket to store your website files.

**CloudFront Distribution:**
Set up a CloudFront distribution to serve the website over HTTPS.
Configure the distribution to point to the S3 bucket as the origin.

**Remote state management:** Use S3 to store Terraform state and DynamoDB for state locking.

# Usage 
**1. Clone the Repository**
```
git clone https://github.com/raziashaik1984/project-Static-website-Hosting

cd project-Static-website-Hosting
```
**2. Initialize Terraform**
```
cd envs/dev

terraform init
```

**3. Review and Apply Changes**
```
terraform plan

terraform apply
```
**4. Testing the Website in a Browser**

Once the Terraform deployment is complete, you should see
`cloudfront_distribution_domain: The CloudFront distribution URL` as output value.

The URL will load your website, serving the `index.html` file from the S3 bucket through CloudFront's global distribution network for optimized performance.

**5. Cleanup**

To remove the infrastructure, run:

```
terraform destroy
```
## Contribution
Feel free to contribute by opening issues or submitting pull requests to improve the project.