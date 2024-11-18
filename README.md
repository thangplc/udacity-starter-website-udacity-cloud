# Deploy Static Website on AWS

In this project, you will deploy a static website to AWS using S3, CloudFront, and IAM.

## Included Files

- `index.html`: The Index document for the website.
- `/img`: The background image file for the website.
- `/vendor`: Bootstrap CSS framework, Font, and JavaScript libraries needed for the website to function.
- `/css`: CSS files for the website.
- `/screenshot`: Image configuration.

## Configuration

- **CloudFront Website**: [https://d3qu5kadvnky1k.cloudfront.net/]
- **Default Hosting Website**: [http://my-static-web-thangplc.s3-website-us-east-1.amazonaws.com/]
- **Bucket Name**: `my-static-web-thangplc`
- **Region**: `us-east-1`
- **User**: `thangplc_dev`
- **Path Folder**: `./`

## Create S3 Bucket

To create the S3 bucket, run the following command:

```bash
aws s3api create-bucket --bucket=${Bucket_name} --region=${Region}
````

## Upload project
To upload the project files to the S3 bucket, use the following command:
```bash
aws s3 sync ${Path_folder} s3://${Bucket_name}/
````
