## Setup

For more details about the ETW input settings, check the [Filebeat documentation](https://www.elastic.co/docs/reference/beats/filebeat/filebeat-input-etw).

### Collecting logs from ETW

[Event Tracing for Windows (ETW)](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-etw.html), a mechanism that allows real-time logging and capturing of Windows system events. This collection can be done either by initiating a new ETW session to gather logs directly from the DNS Server provider or by reading pre-existing logs from a .etl (Event Trace Log) file.

To collect logs via ETW, select **Collect analytical events from Windows ETW**.