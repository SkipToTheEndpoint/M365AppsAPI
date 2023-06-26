| **Data** 	| **Method** 	| **URL** 	| **Example Response** 	| **Notes** 	|
|---	|---	|---	|---	|---	|
| Inventory Summary 	| GET 	| https://query.inventory.insights.office.net/inventory/api/Devices/GetDeviceSummary?api-version=1.1 	|  	|  	|
| Device Builds Summary 	| GET 	| https://query.inventory.insights.office.net/inventory/api/DevicesWithMetadata/GetOfficeBuildDeviceSummaryWithMetadata?api-version=1.1&$count=true 	|  	|  	|
| Device Channels Summary 	| GET 	| https://query.inventory.insights.office.net/inventory/api/DevicesWithMetadata/GetOfficeBuildChannelSummaryWithMetadata?api-version=1.1&$orderby=officeBuildCount%20desc&$count=true 	|  	|  	|