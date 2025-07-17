## Setup
For more details about the GCS input settings, check the [Filebeat documentation](https://www.elastic.co/docs/reference/beats/filebeat/filebeat-input-gcs).

### Collecting logs from GCS

To collect logs via GCS, select **Collect logs via GCS** and configure the following parameters:

- Buckets: This attribute contains the details about a specific bucket like, name, number_of_workers, poll, poll_interval and bucket_timeout. The attribute 'name' is specific to a bucket as it describes the bucket name, while the fields number_of_workers, poll, poll_interval and bucket_timeout can exist both at the bucket level and at the global level. If you have already defined the attributes globally, then you can only specify the name in this yaml config. If you want to override any specific attribute for a specific bucket, then, you can define it here. Any attribute defined in the yaml will override the global definitions. Please see the relevant [Documentation](https://www.elastic.co/guide/en/beats/filebeat/8.5/filebeat-input-gcs.html#attrib-buckets) for further information.
- Project ID: This attribute is required for various internal operations with respect to authentication, creating storage clients and logging which are used internally for various processing purposes.