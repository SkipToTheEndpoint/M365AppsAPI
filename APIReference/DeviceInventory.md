# Device Inventory

Portal Link: https://config.office.com/officeSettings/inventory

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
    <td>Device Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/Devices/GetDeviceSummary?api-version=1.1</td>
    <td>
<pre lang="json">
{
  "totalDevices": 2,
  "officeArchitectureCounts": [
    {
      "officeArchitecture": "X64",
      "count": 2
    }
  ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Device Builds Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/DevicesWithMetadata/GetOfficeBuildDeviceSummaryWithMetadata?api-version=1.1&$count=true</td>
    <td>
<pre lang="json">
{
  "officeBuild": "16.0.16327.20324",
  "installationCount": 1,
  "buildSupportStatus": "Supported",
  "endOfSupportDate": "2023-08-08T00:00:00Z",
  "availabilityDate": "2023-06-13T07:56:08.82Z",
  "officeServicingChannel": "MonthlyEnterpriseChannel"
      },
      {
  "officeBuild": "16.0.16227.20318",
  "installationCount": 1,
  "buildSupportStatus": "Supported",
  "endOfSupportDate": "2023-07-11T00:00:00Z",
  "availabilityDate": "2023-05-09T14:13:34.48Z",
  "officeServicingChannel": "MonthlyEnterpriseChannel"
  }
</pre>
    </td>
  </tr>
  <tr>
    <td>Device Channels Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/DevicesWithMetadata/GetOfficeBuildChannelSummaryWithMetadata?api-version=1.1&$orderby=officeBuildCount%20desc&$count=true</td>
    <td>
<pre lang="json">
{
  "officeServicingChannel": "MonthlyEnterpriseChannel",
  "officeBuildCount": 2,
  "supportedOfficeBuildCount": 2,
  "unsupportedOfficeBuildCount": 0,
  "unknownOfficeBuildCount": 0
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Add-Ins Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/OfficeAddins?api-version=1.1&$orderby=numberOfDevices%20desc&$top=200&$skip=0&$count=false</td>
    <td>
<pre lang="json">
{
  "tenantId": "%TenantID%",
  "name": "Microsoft Data Streamer for Excel",
  "publisher": "Microsoft Corporation",
  "version": "6.8.0.0",
  "numberOfVersions": 1,
  "numberOfDevices": 2
},
{
  "tenantId": "%TenantID%",
  "name": "Microsoft Exchange Add-in",
  "publisher": "",
  "version": null,
  "numberOfVersions": 1,
  "numberOfDevices": 2
}
</pre>
    </td>
  </tr>
</tbody>
</table>