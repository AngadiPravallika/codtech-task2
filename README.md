# CODTECH Task 2 - Wasabi Bucket Policy Proof

## Task Summary
This task required creating a bucket policy for the Wasabi bucket named `task1` to allow public read access.

## Steps Completed:
1. Created bucket `task1` in Wasabi console.
2. Uploaded task file `CODTECH task-1.txt` to the bucket.
3. Created a bucket policy to allow public read access with the following policy JSON:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowAllUsersReadAccess",
      "Effect": "Allow",
      "Principal": {
        "AWS": "*"
      },
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Resource": [
        "arn:aws:s3:::task1",
        "arn:aws:s3:::task1/*"
      ]
    }
  ]
}
