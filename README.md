ASSIGNMENT-Deploy the web application created above on S3 and serve it via cloudfront

SOLUTION-First of all create an AWS account, then Go to the AWS Management Console and sign in to your account.
Click on "Services" in the top navigation bar and select "S3" under the "Storage" category.
Click on the "Create Bucket" button.
Enter a unique name for your bucket in the "Bucket name" field. Note that S3 bucket names must be unique across all AWS accounts, so you may need to try a few different names before finding one that's available.
Select the region where you want to create your bucket. It's important to choose the same region as your CloudFront distribution to minimize latency.
Choose your desired settings for versioning, server access logging, and encryption. These are all optional, so you can leave them at their default values if you're not sure what to choose.
Click the "Create" button to create your new S3 bucket.
Now we have created an S3 bucket. Upload your web application files: Upload your web application files to the S3 bucket you created in the previous step. Ensure that the files are set to public access so that they can be served via CloudFront.
Configure your S3 bucket for static website hosting: In your S3 bucket properties, navigate to the "Static website hosting" section and select "Use this bucket to host a website". Enter the name of your index document and error document, if any.
Create a CloudFront distribution: Create a new CloudFront distribution by navigating to the CloudFront console and selecting "Create Distribution". Select the S3 bucket you created in step 1 as the origin for your distribution.
Configure your CloudFront distribution: In your CloudFront distribution settings, configure the following:
Set the default root object to the name of your index document.
Ensure that your S3 bucket is listed as an origin for your distribution.
Configure caching behavior as needed for your web application.
Update DNS records: Update your DNS records to point to your CloudFront distribution domain name. You can find this domain name in your CloudFront distribution settings.
Test your web application: Once your DNS records have propagated, test your web application by accessing it via your CloudFront distribution domain name.
