# Servicing Profiles

Portal Link: https://config.office.com/officeSettings/serviceprofile

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
    <td>Servicing Profile Details</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/Profiles</td>
    <td>
<pre lang="json">
{
  "id": "%MECSPGUID%",
  "active": true,
  "profileState": 400,
  "profileType": 100,
  "rolloutPipeline": 100,
  "targetChannel": 4
},
{
  "id": "%CurrentSPGUID%",
  "active": false,
  "profileState": 100,
  "profileType": 100,
  "rolloutPipeline": 100,
  "targetChannel": 1
},
{
  "id": "%SACSPGUID%",
  "active": false,
  "profileState": 100,
  "profileType": 100,
  "rolloutPipeline": 100,
  "targetChannel": 2
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Profile Rules</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/%SPGUID%/rules</td>
    <td>
<pre lang="json">
{
  "profileId": "%SPGUID%",
  "rulesList": {
    "valueRules": [
        {
          "value": "3",
          "id": "%IDGUID%",
          "name": "ServicingDeadline",
          "ruleType": 200,
          "frequency": 500
        }
    ],
    "scopedValueRules": [
        {
          "scopedToAllProfileDevices": true,
          "scopedAADGroups": [],
          "scopedDevices": null,
          "value": null,
          "id": "%IDGUID%",
          "name": "Group",
          "ruleType": 100,
          "frequency": 500
        },
        {
          "scopedToAllProfileDevices": false,
          "scopedAADGroups": [
              "%AADGroupGUID%"
            ],
          "scopedDevices": null,
          "value": "{\"waveId\": 1, \"nextWaveStartInDays\":3}",
          "id": "%IDGUID%",
          "name": "Wave",
          "ruleType": 200,
          "frequency": 500
        },
        {
          "scopedToAllProfileDevices": false,
          "scopedAADGroups": [
              "%AADGroupGUID%"
            ],
          "scopedDevices": null,
          "value": "{\"waveId\": 2, \"nextWaveStartInDays\":3}",
          "id": "%IDGUID%",
          "name": "Wave",
          "ruleType": 200,
          "frequency": 500
        }
    ],
    "excludedValueRules": [],
    "expressionRules": [
        {
          "property": "DiskSpace",
          "expressionOperator": "GreaterThanOrEqual",
          "value": "0",
          "id": "%IDGUID%",
          "name": "DiskSpace",
          "ruleType": 100,
          "frequency": 100
        },
        {
          "property": "OfficeServicingChannel",
          "expressionOperator": "IsIn",
          "value": "BetaChannel,CurrentChannelPreview,CurrentChannel,MonthlyEnterpriseChannel,SemiAnnualEnterpriseChannelPreview,SemiAnnualEnterpriseChannel",
          "id": "%IDGUID%",
          "name": "Channel",
          "ruleType": 100,
          "frequency": 100
        },
        {
          "property": "OfficeServicingChannel",
          "expressionOperator": "IsMatch",
          "value": "MonthlyEnterpriseChannel",
          "id": "%IDGUID%",
          "name": "Channel",
          "ruleType": 200,
          "frequency": 100
        }
    ]
  }
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Upcoming Release</td>
    <td>GET</td>
    <td>https://clients.config.office.net/releases/v1.0/NextReleaseVersion/MonthlyEnterpriseChannel</td>
    <td>
<pre lang="json">
{
  "releaseVersion": 2305,
  "availabilityDate": "2023-07-11T00:00:00Z"
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Current Release</td>
    <td>GET</td>
    <td>https://clients.config.office.net/releases/v1.0/LatestRelease/MonthlyEnterpriseChannel?releaseType=feature</td>
    <td>
<pre lang="json">
{
  "id": 447,
  "channel": 4,
  "channelId": "%ChannelName%",
  "releaseVersion": 2304,
  "releaseType": 1,
  "availabilityDate": "2023-06-13T07:56:08.82Z",
  "endOfSupportDate": "2023-08-08T00:00:00Z",
  "buildVersion": {
      "major": 16,
      "minor": 0,
      "build": 16327,
      "buildRevision": 20324,
      "buildVersionString": "16.0.16327.20324"
  },
  "releaseRank": "1",
  "kbLink": "https://technet.microsoft.com/en-us/office/mt465751.aspx",
  "cdnBaseUrl": "http://officecdn.microsoft.com/pr/55336b82-a18d-4dd6-b5f6-9e5095c314a6"
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Rollout Summary</td>
    <td>GET</td>
    <td>https://clients.config.office.net/rolloutProgress/v1.0/rolloutProgress/%SPGUID%/MonthlyEnterpriseChannel/%buildVersionString%/summary</td>
    <td>
<pre lang="json">
{
  "0": 2,
  "1": 0,
  "2": 1,
  "4": 0,
  "5": 0
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Rollout Issues</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/%buildVersionString%/Issues</td>
    <td>
<pre lang="json">
{
  "serviceProfileId": "%SPGUID%",
  "issues": [],
  "skipToken": "",
  "count": 0
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Rollout Progress</td>
    <td>GET</td>
    <td>https://clients.config.office.net/rolloutProgress/v1.0/rolloutProgress/%SPGUID%/MonthlyEnterpriseChannel/%buildVersionString%/devices?top=50</td>
    <td>
<pre lang="json">
{
  "profileId": "%SPGUID%",
  "skipToken": "",
  "collectionIndex": 1,
  "count": 1,
  "devices": [
    {
      "deviceId": "%DeviceID%",
      "name": "%DeviceName%",
      "currentVersion": "16.0.16327.20324",
      "lastSeen": "2023-06-22T18:44:07.034159",
      "updateStatus": 2,
      "inventoryDeviceStatus": 0,
      "customWaveId": 3,
      "aadUserName": "%UserPrincipalName%",
      "officeReleaseVersion": "2304"
    }
  ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Wave Progress</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/4/%buildVersionString%/waveprogress</td>
    <td>
<pre lang="json">
{
  "waves": [
    {
      "projectedCount": 1,
      "updatedCount": 0,
      "displayInfo": 0
    },
    {
      "projectedCount": 0,
      "updatedCount": 0,
      "displayInfo": 1
    },
    {
      "projectedCount": 2,
      "updatedCount": 1,
      "displayInfo": 2
    }
    ],
  "rolloutDeadline": 4
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Device Rollbacks</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/MEC/%buildVersionString%/rollbackLinkedGroups</td>
    <td>
<pre lang="json">
{
  "entities": [],
  "profileId": "%SPGUID%"
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Exclusion Windows</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/servicingExclusionWindows</td>
    <td>
<pre lang="json">
{
  []
}
</pre>
    </td>
  </tr>
</tbody>
</table>