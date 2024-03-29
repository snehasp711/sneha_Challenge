# sneha_Challenge
static web application in AWS

**Step 1: Set up an S3 Bucket for Hosting
Create an S3 Bucket:**
-Log in to the AWS Management Console.
-Navigate to the S3 service.
-Click on "Create bucket".
-Choose a globally unique bucket name and specify the region.
-Leave other settings as default and create the bucket.
Step 2: Upload Static Content to S3 Bucket
**Create HTML File:
Create an HTML file named index.html**
**Upload HTML File to S3:**
-Select the newly created S3 bucket.
-Click on "Upload" and select the index.html file.
-Ensure that the file is publicly accessible by configuring the permissions.
**Step 3: Enable Static Website Hosting on S3**
-Configure Static Website Hosting:
-Select the bucket in the S3 console.
-Navigate to the "Properties" tab.
-Click on "Static website hosting".
-Choose "Use this bucket to host a website" and specify index.html as the index document.
-Save the configuration.
**Step 4: Configure SSL/TLS Certificate with ACM**
-Request SSL/TLS Certificate:
-Navigate to the AWS Certificate Manager (ACM) service.
-Click on "Request a certificate".
-Enter your domain name and follow the steps to complete the request.
-Choose DNS validation method and add the required DNS records to your DNS provider.
**Step 5: Configure CloudFront Distribution**
-Create CloudFront Distribution:
-Navigate to the CloudFront service.
-Click on "Create Distribution".
-Choose "Web" as the delivery method.
-Configure the origin settings to point to the S3 bucket.
-Specify the ACM certificate for SSL/TLS.
-Configure additional settings such as caching behavior and access control.
-Save the configuration and wait for the distribution to deploy.
**Step 6: Implement Automated Deployment with Java**
-Use AWS SDK for Java:
-Add AWS SDK for Java dependency to your project (Maven or Gradle).
-Use AWS SDK APIs to interact with S3, CloudFront, and ACM programmatically.
-Write Java code to automate the deployment process, including uploading static content to S3, configuring CloudFront distribution, and associating ACM certificate.
**Step 7: Develop and Apply Automated Tests**
**Write Automated Tests:**
-Use testing frameworks such as JUnit or TestNG to write automated tests.
-Write tests to validate HTTPS redirection, content availability, and security headers.
-Use AWS SDK or HTTP client libraries to perform HTTP requests and assertions in tests.
-Automate test execution as part of your CI/CD pipeline.
