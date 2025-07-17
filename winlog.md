## Setup

For more details about the Winlog input settings, check the [Filebeat documentation](https://www.elastic.co/docs/reference/beats/filebeat/filebeat-input-winlog).

### Collecting logs from Winlog

The `winlog` input package for Elastic, is dedicated to collecting Windows event logs. It utilizes Windows APIs to read events from various logs such as Application, Security, and System.

To collect logs via Winlog, select **Collect logs via Winlog** and configure the following parameters:

- Event IDs: A list of included and excluded (blocked) event IDs. The value is a comma-separated list. The accepted values are single event IDs to include (e.g. 4624), a range of event IDs to include (e.g. 4700-4800), and single event IDs to exclude (e.g. -4735). Limit 22 IDs.