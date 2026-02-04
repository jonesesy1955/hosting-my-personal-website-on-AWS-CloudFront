# Migrating and deploying a static website on S3, CloudFront

# Why this project?
This was a project to develop AWS cloud skills. I'm taking a cloud architecture class to prepare for the AWS SAA exam in December. One of the side projects to increase our class expertise was to create a personal website and host it using AWS CloudFront. This was my first hands on experience with doing an AWS project. 

# Resources
I watched several YouTube tutorials since this is widely recommended project for people interested in learning more about AWS.
https://www.youtube.com/watch?v=lB4DTqMEumY&list=PL6qdJ78d0B78gb4rrRQ-XJR2BhbgTre6L&index=9

- This was the main video I used. It took my through almost the entire process before I ran into any issues.

Here are a few others I watched: 
https://youtu.be/mirW9pBann8?si=smi93Cl1SoOnXOxu

https://youtu.be/X9cdkqBgLbs?si=2aBhJteiiAmQkect

# Steps 
1. Download the resources in the BootStrap Template for my static pages.
2. In the AWS Console, go to S3 and create a S3 bucket with a unique name.
3. Select the bucket name. Click _Upload_, _add files_, and select the files downloaded from the Bootstrap Template to upload.
4. Under the Permissions tab, clear the check mark on _Block all public access_ to allow the internet to access the website. Created a bucket policy.
5. Under Properties, enable _S3 static web hosting_ to check the website is deployed. 
6. In the AWS Console, go to Route 53 > Hosted zones > Create hosted zone

# Challenges 
The main video showed me how to use a CloudFront created domain name. However, I had purchased a domain name and wanted to use that domain instead. I ran into issues configuring the bucket policies correctly
