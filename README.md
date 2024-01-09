<h1>Building a Serverless Web Application on AWS</h1>

<h2>Description:</h2>

- <b>Create a DynamoDB table to store the items<b/>
- <b>Build a Lambda function to handle the CRUD operations on the DynamoDB table<b/>
- <b>Use S3 to store and host the web application's static files (HTML, CSS, and JavaScript).<b/>
- <b>Create a CloudFront distribution to serve the S3-hosted static files with low latency<b/>

<h2>Project Architecture</h2>

<p align="center">
 <img src="https://i.imgur.com/R9BgYDN.png" height="80%" width="80%" />

<h2>Objectives:</h2>

- <b>Gain hands-on experience building a serverless application using AWS Lambda, DynamoDB, S3, CloudFront<b/>
- <b>Improve skills in cloud computing, serverless architecture, and AWS services<b/>

<h2>Languages and Utilities Used:</h2>

- <b>AWS Free Tier </b> 

<h2>Program Overview:</h2>

Based on the infrastructure layout, the lab will be broken down into the following sections:<br/>

[Step 1] Creating AWS S3 Bucket <br/> 

[Step 2] Configuration of AWS Cloudfront<br/> 

[Step 3] Configuration of AWS Route53 & AWS Certificate Manager<br/> 

[Step 4] AWS DynamaDB<br/> 

[Step 5] Creation of AWS Lambda Function and Integration with Dynamo DB<br/> 

[Step 6] Serverless Web Application Testing<br/> 

<h2>Program walk-through:</h2>

<p align="center">
<b>[Step 1] Creating AWS S3 Bucket</b> <br/>
S3 Bucket is where we will store our static files.<br/>
<br/>
 1. Create a new S3 bucket and ensure 'Block all public access to bucket' settings is toggled on. <br/>
 <img src="https://i.imgur.com/KmSarYF.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/mckEv3X.png" height="80%" width="80%" /><br/>
<br/>
 2. Add web application files (HTML,css.JavaScript) into our newly created S3 Bucket.
 <img src="https://i.imgur.com/V9H5iw3.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/U8Z8Qx6.png" height="80%" width="80%" /><br/>
<br/>

<p align="center">
<b>[Step 2] Configuration of AWS Cloudfront<br/>
Cloudfront distribution is needed to serve S3 static files with low latency. <br/>
<br/>
 1. Create a new Cloudfront distribution with 'Origin Access Control' settings to only allow access to our S3 bucket from Cloudfront. <br/>
 <img src="https://i.imgur.com/95TZU8S.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/BLe8Der.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/7LvdjsW.png" height="80%" width="80%" /><br/>
<br/>
<b></b>Allow S3 Bucket access to Cloudfront distribution via Bucket policy <br/>
 2. Retrieve bucket policy in newly created Cloudfront distribution under 'Origins' tab.
 <img src="https://i.imgur.com/3yMH1nz.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/kPpvHX2.png" height="80%" width="80%" /><br/>
<br/>
 3. Paste the policy statement into our S3 bucket 'Permissions' tab.<br/>
 <img src="https://i.imgur.com/BxVoeY6.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/kV4GEJG.png" height="80%" width="80%" /><br/>
<br/>
 4. Next, in our Cloudfront distribution, we need to define a root object. In this case it will be our html file name. 
 <img src="https://i.imgur.com/gHoeyMM.png" height="80%" width="80%" /><br/>
 <img src="https://i.imgur.com/29gKWvZ.png" height="80%" width="80%" /><br/>




















 
