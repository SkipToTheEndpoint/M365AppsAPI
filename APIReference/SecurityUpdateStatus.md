# Security Update Status

Portal Link: https://config.office.com/officeSettings/currency

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
    <td>Security Update Status Metrics</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/SecurityCurrencyDevices/GetSecurityUpdateStatusMetrics?api-version=1.1</td>
    <td>
<pre lang="json">
{
    "securityCurrencyDevicesWithAppsTotal": 2,
    "securityCurrencyUpToDateDevicesTotal": 1,
    "securityCurrencyNotUpToDateDevicesTotal": 1,
    "securityCurrencyUnknownStatusDevicesTotal": 0
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Security Update Status Metrics by Channel</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/SecurityCurrencyDevices/GetSecurityUpdateStatusMetricsByChannel?api-version=1.1</td>
    <td>
<pre lang="json">
{
    "value": [
        {
    "officeServicingChannel": "MonthlyEnterpriseChannel",
    "securityCurrencyDevicesWithAppsTotal": 2,
    "securityCurrencyUpToDateDevicesTotal": 1,
    "securityCurrencyNotUpToDateDevicesTotal": 1,
    "securityCurrencyUnknownStatusDevicesTotal": 0
        }
    ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Security Update Goal</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/SecurityCurrencyGoal?api-version=1.1</td>
    <td>
<pre lang="json">
{
    "securityCurrencyGoalId": "%GoalIDGUID%",
    "securityCurrencyGoalTimeInDays": 14,
    "securityCurrencyGoalPercentage": 90,
    "securityCurrencyGoalRemainingDays": 0
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Devices Not Up To Date</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/SecurityCurrencyDevices?api-version=1.1&$filter=(securityCurrencyStatus%20eq%20%27NotUpToDate%27)&$top=200&$skip=0&$count=false</td>
    <td>
<pre lang="json">
{
    "deviceId": "%DeviceID%",
    "name": "%DeviceName%",
    "lastSeen": "2023-06-11T21:00:16.1788037Z",
    "globalDeviceId": "%GlobalDeviceID%",
    "serviceabilityManagerDeviceId": "",
    "aadDeviceId": "%AADDeviceID%",
    "osBuildVersion": "10.0.22621.1702",
    "osFamily": "Windows",
    "osReleaseVersion": "22H2",
    "totalRamInGigaBytes": 7.91,
    "processorArchitecture": "X64",
    "manufacturer": "Microsoft Corporation",
    "model": "Virtual Machine",
    "modelFamily": "Virtual Machine",
    "freeDiskSpaceInGigabytes": 89.6,
    "totalDiskSpaceInGigaBytes": 126.22,
    "natIpAddress": "",
    "networkRegion": "",
    "networkCost": "Unknown",
    "officeArchitecture": "X64",
    "officeAudienceGroup": "Production",
    "officeAudienceID": "Production_MEC",
    "officeDownloadSource": null,
    "officeMacroEnabledFilesInMRU": false,
    "officeReleaseVersion": "2303",
    "officeServicingChannel": "MonthlyEnterpriseChannel",
    "officeAddinCategorization": "NonInboxAddins",
    "officeBuildVersion": "16.0.16227.20318",
    "officeInventoryAddonVersion": "16.0.16227.20202",
    "status": "Active",
    "aadUserDisplayName": "%DisplayName%",
    "aadUserName": "%UserPrincipalName%",
    "aadUserId": "%AADUserID%",
    "previousUpdateChannel": "Unknown",
    "autoProvisionUserId": "%AADUserID%",
    "ignoreGpo": null,
    "licenseId": null,
    "notificationUrl": null,
    "officeManagementStateDetail": "Unsupported",
    "tenantId": "%TenantID%",
    "securityCurrencyStatus": "NotUpToDate"
        }
</pre>
    </td>
  </tr>
</tbody>
</table>