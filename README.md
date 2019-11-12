# CloudGenix Get Events (Preview)
This utility is used to download events from the CloudGenix managed network to a CSV file.

#### Synopsis
Enables downloading of alarms and alerts raised on the CloudGenix managed network. The user can filter events by Site, event codes and based on the start time.


#### Requirements
* Active CloudGenix Account
* Python >= 2.7 or >=3.6
* Python modules:
    * CloudGenix Python SDK >= 5.1.1b1 - <https://github.com/CloudGenix/sdk-python>

#### License
MIT

#### Installation:
 - **Github:** Download files to a local directory, manually run `getevents.py`. 

### Examples of usage:
Get events from a site:
```
./getevents.py -S Sitename 
```
Get events from a multiple sites:
``` 
./getevents.py -S Site1,Site2,Site3
```
Get events for specific event codes:
```angular2
./getevents.py -EC NETWORK_VPNLINK_DOWN,NETWORK_DIRECTINTERNET_DOWN
```

Use the -H hours to specify the time delta in hours for the event query.

Help Text:
```angular2
Tanushrees-MacBook-Pro:getevents tanushreekamath$ ./getevents.py -h
usage: getevents.py [-h] [--controller CONTROLLER] [--email EMAIL]
                    [--pass PASS] [--eventcodes EVENTCODES] [--hour HOUR]
                    [--sitename SITENAME]

CloudGenix: Get Events Script.

optional arguments:
  -h, --help            show this help message and exit

API:
  These options change how this program connects to the API.

  --controller CONTROLLER, -C CONTROLLER
                        Controller URI, ex. C-Prod:
                        https://api.elcapitan.cloudgenix.com

Login:
  These options allow skipping of interactive login

  --email EMAIL, -E EMAIL
                        Use this email as User Name instead of prompting
  --pass PASS, -P PASS  Use this Password instead of prompting

Filters for events:
  The following attributes will be used to query events

  --eventcodes EVENTCODES, -EC EVENTCODES
                        List event codes you want to query for
  --hour HOUR, -H HOUR  Number of hours from now you need the events queried
                        for
  --sitename SITENAME, -S SITENAME
                        Name of the Site you want events filtered for. For
                        multiple sites, separate names by using a comma.
```

#### Version
| Version | Build | Changes |
| ------- | ----- | ------- |
| **1.0.0** | **b1** | Initial Release. |


#### For more info
 * Get help and additional CloudGenix Documentation at <http://support.cloudgenix.com>
 