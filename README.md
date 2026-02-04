# Description
This was my first project working with AWS. The goal was to deploy a static website using S3 and CloudFront to post my resume. 

# Resources
I watched several YouTube tutorials since this is widely recommended project for people interested in learning more about AWS. This was the main video I used. It took my through almost the entire process before I ran into any issues.

https://www.youtube.com/watch?v=lB4DTqMEumY&list=PL6qdJ78d0B78gb4rrRQ-XJR2BhbgTre6L&index=9

Here are a few others I watched: 

https://youtu.be/mirW9pBann8?si=smi93Cl1SoOnXOxu

https://youtu.be/X9cdkqBgLbs?si=2aBhJteiiAmQkect

# AWS Resources
S3  
CloudFront  
Route 53   
Certificate Manager  

# Steps 
1. Download the resources in the BootStrap Template for my static pages.
2. In the AWS Console, go to S3 and create a S3 bucket with a unique name.
3. Select the bucket name. Click _Upload_, _add files_, and select the files downloaded from the Bootstrap Template to upload.
4. Under the Permissions tab, clear the check mark on _Block all public access_ to allow the internet to access the website. Created a bucket policy.
5. Under Properties, enable _S3 static web hosting_ to check the website is deployed. 
6. In the AWS Console, go to Route 53 > Hosted zones > Create hosted zone
7. Entered my domain 
8. Copied the custom nameservers from Squarespace where the domain is hosted and replaced the default nameservers (NS) records in AWS
9. In the AWS Console, go to Certificate Manager > Request certficiate > Request a public certificate. 
10. Entered my domain, then selected _Create a record in Route 53_. Verified the record was created in Route 53. 
11. In the AWS Console, go to CloudFront > Create distribution
12. For the origin, copied the URL from my bucket under Permissions > Static website hosting.
13. Configured the distribution as following: selected _Redirect from HTTP to HTTPS_, insert the domain name under _Alternate Domain Names (CNAMEs)_, selected _Custom SSL certificate_
14. Verified the CloudFront domain name can be accessed
15. In the AWS Console, go to Route 53 > Hosted zones > Create record > A type > Record name, paste the CloudFront domain name. Create record

# Challenges 
The main video showed me how to use a CloudFront created domain name. However, I had purchased a domain name and wanted to use that domain instead. I ran into issues configuring the bucket policies correctly. 
