Steps taken to setup infrastructure manually:

S3 Bucket Creation:
1. Create bucket with globally unique name - in this case I set it to be of website-zacharyjanssen.com (registered domain name)
2. Uncheck "Block all public access"
3. Create Bucket
4. After bucket creation, I went into the properties of the bucket, scrolled all the way down, and enabled "Static Website Hosting"
5. Next, I went to the permissions tab of the bucket and added the bucket policy to allow public read access 

BUCKET POLICY:
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadAccess",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::BUCKET_NAME/*"
        }
    ]
}

