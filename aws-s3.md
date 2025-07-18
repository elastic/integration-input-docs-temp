## Setup

Set up an Amazon S3
- Create an Amazon S3 bucket. Refer to the link [here](https://docs.aws.amazon.com/AmazonS3/latest/userguide/create-bucket-overview.html).
- User can set the parameter "Bucket List Prefix" according to the requirement.

- **AWS S3 polling mode**: Writes data to S3, and Elastic Agent polls the S3 bucket by listing its contents and reading new files. 
- **AWS S3 SQS mode**: Writes data to S3; S3 sends a notification of a new object to SQS; the Elastic Agent receives the notification from SQS and then reads the S3 object. Multiple agents can be used in this mode.


### Collecting logs from S3 bucket

When log collection from an S3 bucket is enabled, you can access logs from S3 objects referenced by S3 notification events received through an SQS queue or by directly polling the list of S3 objects within the bucket.

The use of SQS notification is preferred: polling list of S3 objects is
expensive in terms of performance and costs and should be used only
when no SQS notification can be attached to the S3 buckets. This input
integration also supports S3 notification from SNS to SQS.

To enable the SQS notification method, set the `queue_url` configuration value. To enable the S3 bucket list polling method, configure both the `bucket_arn` and number_of_workers values. Note that `queue_url` and `bucket_arn` cannot be set simultaneously, and at least one of these values must be specified.

NOTE: To access SQS and S3, these [specific AWS permissions](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-aws-s3.html#_aws_permissions_2) are required.

  To collect logs via AWS S3, enter the following details:
  - Collect logs via S3 Bucket toggled on
  - Access Key ID
  - Secret Access Key
  - Bucket ARN or Access Point ARN
  - Session Token

  Alternatively, to collect logs via AWS SQS, enter the following details:
  - Collect logs via S3 Bucket toggled off
  - Queue URL
  - Secret Access Key
  - Access Key ID
  - Session Token
