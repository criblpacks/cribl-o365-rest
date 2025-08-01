# O365 Rest Collector
----

## About this Pack

This pack is designed to handle JSON data collected from the Office 365 Message Trace collector source. The JSON is parsed and the timestamp normalized from the proper field within each event. 

The pack also currently includes three forms of outputs:

1. Normalized JSON
2. OCSF - Primarily meant for Amazon Security Lake, the pack normalizes the data into the proper OCSF category.
3. Splunk - default index and sourcetype supplied from Knowledge > Variables, but can be overwritten in pipeline


## Deployment

The O365 Rest Collector pack allows for events to be sent from the O365 Message Trace API endpoint and normalized into the proper format for the required destinations. To use this pack, follow these steps:

1. Configure the Pack This pack includes several functions that can help reduce events. Please make sure you evaluate the functions before enabling, to ensure vital data is not missed. 

2. Configure the Office 365 Message Trace Source, detailed instructions for configuring the source can be found at https://docs.cribl.io/stream/sources-office365-msg-trace/

3. Connect the Pack to the Office 365 Message Trace source on the Global Routes page where you can add a new route, specify a filter expression for the new Office 365 Message Trace source and choose the cribl-o365-rest pack in the Pipeline dropdown.

Additionally, several output formats are available to be selected. Please only enable one output, as enabling multiple may break the output formatting.

## Release Notes

### Version 0.1.0
Initial release

## Contributing to the Pack

To contribute to the Pack, please connect with us on [Cribl Community Slack](https://cribl-community.slack.com/). You can suggest new features or offer to collaborate.

## License
This Pack uses the following license: [Apache 2.0](https://github.com/criblio/appscope/blob/master/LICENSE).