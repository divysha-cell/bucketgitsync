# Connector_22_QRadar
Qradar Baseline Offenses connector used to fetch offenses and create Chronicle SOAR alerts based on the Qradar offenses names. Connector will create a single SOAR alert per Qradar offense, and will not try to create additional SOAR alerts with new events from Qradar. Connector uses SOAR dynamic list, but by default if no whitelist rules are set, it will fetchingest all offenses returned from the Qradar API offenses. Connector requires Qradar API version 10.1 or higher.


Integration: QRadar

Integration Version: 67

Device Product Field: deviceProduct

Event Name Field: EventName
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is default environment|False|dummy_valid_string|
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.|False|.*|
|API Root|The API server address.|True|https://127.0.0.1|
|API Token|The API authentication token.|True|*****|
|API Version|The Qradar API version to be used, the Connector supports API version starting from 10.1.|True|10.1|
|Total limit of events per offense|Specify how many events per Qradar offense should be ingested in total by connector, after reaching that limit  new events will not be ingested for the offense.|True|100|
|Connector Events Page Size|The size of the page that connector will use to process events in batches.|True|100|
|Max Offenses per Cycle|Max offenses to process per connector run. Note: it’s not recommended to put a value lower than 10.|True|10|
|Max Days Backwards|Number of days before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|1|
|Offenses Padding Period|Time frame in minutes to fetch offenses in minutes.|True|60|
|Events Padding Period|Time frame in days to fetch events data.|True|1|
|Events Limit per Qradar Offence Rule|Specify an optional limit for how many events should be ingested per single rule in Qradar offense, no new events will be ingested to the offense for the related Qradar rule once this limit is reached. Limit cant be bigger than 'Total limit of events per offense'.|False|10|
|Custom Fields|Custom fields that configured by the user at the QRadar, comma separated, e.g: Field A,Field B|False|dummy_valid_string|
|Domain Filter|Specify Qradar domains from which offenses should be ingested. If no values are provided, the connector will ingest offenses from all domains. Parameter accepts multiple values as a comma separated string.|False|dummy_valid_string|
|Magnitude Filter|Specify an offense magnitude to ingest, offenses with the magnitude equal or bigger than provided will be ingested to Siemplify.|False|10|
|Proxy Server Address|The address of the proxy server to use.|False|https://127.0.0.1|
|Proxy Username|The proxy username to authenticate with.|False|dummy_valid_string|
|Proxy Password|The proxy password to authenticate with.|False|*****|
|What Value to use for the Name Field of Siemplify Alert?|Specify what format to follow to generate names for the alerts created by the connector. Possible values are: custom_alert_name or offense_description.|False|custom_alert_name|
|Use dynamic list as a blocklist|If enabled, dynamic lists will be used as a blocklist. If the checkbox is not enabled and no allow rules are set, the connector will fetch all offenses returned from the Qradar API.|False|false|
|Disable Overflow|If enabled, connector overflow mechanism will not be checked for the created alerts - “overflow” alerts will not be created, connector will try to fetch all offenses returned from the Qradar.|False|false|
|Qradar Offense Rules Re-Sync Timer|Specify in minutes how often connector should re-sync Qradar offense rules list. If empty value or 0 is specified, connector will do re-sync every run.|False|10|
|Debug Logging|If enabled, connector will write detailed messages of its execution to the log file.|False|false|
|Create SOAR alerts for offenses with 0 events|If enabled, connector will create a SOAR alert using the Qradar offense data for both alert and event for offenses that were fetched with no events.|False|false|
|Offenses Creation Timer (minutes)|Specify the amount of time in minutes to pass before the connector will try to fetch events data for the newly created Qradar offense. If the connector failed to get the events after the configured amount of time have passed, and if the "Create SOAR alerts if failed to get events for it?" parameter is enabled, the connector will use the fallback to create SOAR alert and event from the same Qradar offense data.|False|5|

