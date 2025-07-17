## Setup

For more details about the CEL input settings, check the [Filebeat documentation](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-cel.html).

### Collecting logs from CEL

To collect logs via CEL, select **Collect logs via CEL** and configure the following parameters:

- Dataset name: Dataset to write data to. Changing the dataset will send the data to a different index. You can't use `-` in the name of a dataset and only valid characters for [Elasticsearch index names](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-index_.html).
- OAuth2 Client ID: Client ID used for OAuth2 authentication
- OAuth2 Client Secret: Client secret used for OAuth2 authentication
- OAuth2 Token URL: The URL endpoint that will be used to generate the tokens during the oAuth2 flow. It is required if no oauth_custom variable is set or provider is not specified in oauth_custom variable.
- Resource URL: i.e. scheme://host:port/path