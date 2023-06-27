# OneDrive

Portal Link: https://config.office.com/officeSettings/onedrive

The below table contains a selection of API endpoints and responses. Data such as GUIDs have been replaced with generic variable names where appropriate.

<table>
<thead>
  <tr>
    <th>Data</th>
    <th>Method</th>
    <th>URL</th>
    <th>Example Response</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Tenant Association Key</td>
    <td>GET</td>
    <td>https://clients.config.office.net/endpointprovisionhealth/v1.0/tenantassociation</td>
    <td>
<pre lang="json">
{
    "tenantAssociationJwt": "%TAK%",
    "enabled": true
}
</pre>
    </td>
  </tr>
  <tr>
    <td>OneDrive Sync Health Summary</td>
    <td>GET</td>
    <td>https://clients.config.office.net/odbhealth/v1.0/synchealth/reports/count</td>
    <td>
<pre lang="json">
{
  "0":2,
  "1":2,
  "2":0,
  "3":0,
  "4":2,
  "5":0,
  "6":0
}
</pre>
    </td>
  </tr>
  <tr>
    <td>OneDrive Sync Health Issues</td>
    <td>GET</td>
    <td>https://clients.config.office.net/odbhealth/v1.0/synchealth/issues</td>
    <td>
<pre lang="json">
{
  []
}
</pre>
    </td>
  </tr>
  <tr>
    <td>OneDrive Sync Client Version</td>
    <td>GET</td>
    <td>https://clients.config.office.net/odbhealth/v1.0/synchealth/reports/versioncount</td>
    <td>
<pre lang="json">
{
   "updateRing": 4,
   "currentOneDriveVersion": "23.129.0620.0001",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 1,
   "oneDrivePlatformType": 0
},`
{
   "updateRing": 5,
   "currentOneDriveVersion": "23.119.0606.0001",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 1,
   "oneDrivePlatformType": 0
},
{
   "updateRing": 0,
   "currentOneDriveVersion": "23.061.0319.0003",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 0,
   "oneDrivePlatformType": 0
},
{
   "updateRing": 4,
   "currentOneDriveVersion": "23.129.0620.0001",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 0,
   "oneDrivePlatformType": 1
},
{
   "updateRing": 5,
   "currentOneDriveVersion": "23.119.0606.0001",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 0,
   "oneDrivePlatformType": 1
},
{
   "updateRing": 0,
   "currentOneDriveVersion": "23.061.0319.0003",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 0,
   "oneDrivePlatformType": 1
},
{
   "updateRing": 6,
   "currentOneDriveVersion": "",
   "newerCount": 0,
   "currentCount": 0,
   "olderCount": 0,
   "oneDrivePlatformType": 2
}
</pre>
    </td>
  </tr>
  <tr>
    <td>OneDrive Sync Health Report Top 50</td>
    <td>GET</td>
    <td>https://clients.config.office.net/odbhealth/v1.0/synchealth/reports?top=50&orderby=UserName%20asc</td>
    <td>
<pre lang="json">
{
  "type": "odb",
  "schemaVersion": "1.0",
  "oneDriveDeviceId": "%ODDeviceID%",
  "userName": "%DisplayName%",
  "userEmail": "%UserPrincipalName%",
  "deviceName": "%DeviceName%",
  "oneDriveVersion": "23.107.0521.0001",
  "updateRing": 5,
  "osName": "Windows",
  "osVersion": "10.0.22621",
  "oneDriveBuildType": "",
  "kfmState": 60,
  "kfmOptInWithWizardGPOEnabled": false,
  "kfmSilentOptInGPOEnabled": true,
  "kfmFolders": [
    3,
    1,
    2
  ],
  "kfmFolderCount": 3,
  "lastUpToDateSyncTimestamp": "2023-06-07T12:51:07Z",
  "reportTimestamp": "2023-06-11T07:58:13Z",
  "totalErrorCount": 0,
  "errorDetails": [],
  "errorKeys": [],
  "HasAttachments": false,
  "ContentSourceApplication": null
}
</pre>
    </td>
  </tr>
</tbody>
</table>