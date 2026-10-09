# Static Website Deployment Using Amazon S3 and CloudFront

## Project Overview

This project involved deploying a static website using Amazon S3 for storage and Amazon CloudFront for content delivery.

## AWS Services Used

* **Amazon S3:** Stored the website's HTML, CSS, JavaScript, and image files.
* **Amazon CloudFront:** Delivered website content to users while allowing the S3 bucket to remain private.

## Implementation

1. Created an S3 bucket to store the website files.
2. Uploaded the website's `index.html`, `assets/`, and `images/` files.
3. Kept S3 Block Public Access enabled.
4. Created a CloudFront distribution connected to the S3 bucket.
5. Configured private access between CloudFront and S3 using a bucket policy.
6. Set `index.html` as the default root object.
7. Tested the deployed website through the CloudFront distribution domain.

## Security Measures

* Blocked public access to the S3 bucket.
* Allowed CloudFront to retrieve objects using `s3:GetObject`.
* Restricted the bucket policy to the intended CloudFront distribution.

## Lessons Learned

* How Amazon S3 stores static website files.
* How CloudFront delivers content from an S3 origin.
* How to serve a website without making the S3 bucket publicly accessible.
* How bucket policies can restrict access to a specific CloudFront distribution.
* How to distinguish website asset differences from infrastructure problems during troubleshooting.

## Future Improvements

* Rebuild the infrastructure independently.
* Recreate the deployment using Terraform.
* Add custom domain and HTTPS configuration.
* Review AWS costs and resource cleanup procedures.
