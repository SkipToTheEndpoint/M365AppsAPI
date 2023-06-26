<table>
<thead>
  <tr>
    <th>Data</th>
    <th>Method</th>
    <th>URL</th>
    <th>Example Response</th>
    <th>Notes</th>
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
    "id": "%SPGUID%",
    "active"": false,
    "profileState"": 0,
    "profileType"": 0,
    "rolloutPipeline"": 0,
    "targetChannel"": 4
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Profile Rules</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/%SPGUID%/rules</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Upcoming Release</td>
    <td>GET</td>
    <td>https://clients.config.office.net/releases/v1.0/NextReleaseVersion/MonthlyEnterpriseChannel</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Current Release</td>
    <td>GET</td>
    <td>https://clients.config.office.net/releases/v1.0/LatestRelease/MonthlyEnterpriseChannel?releaseType=feature</td>
    <td>
<pre lang="json">
{
    "id": 444,
    "channel": 4,
    "channelId": 
    "MonthlyEnterprise",
    "releaseVersion": 2210,
    "releaseType": 1,
    "availabilityDate": "2022-12-13T10:01:13.853Z",
    "endOfSupportDate": "2023-02-14T00:00:00Z",
    "buildVersion": {
        "major": 16,
        "minor": 0,
        "build": 15726,
        "buildRevision": 20262,
        "buildVersionString": "16.0.15726.20262"
        },
    "releaseRank": "1",
    "kbLink": "<a href="https://technet.microsoft.com/en-us/office/mt465751.aspx&quot;,&quot;cdnBaseUrl&quot;">https://technet.microsoft.com/en-us/office/mt465751.aspx"</a>,
    "cdnBaseUrl"</a>: "<a href="http://officecdn.microsoft.com/pr/55336b82-a18d-4dd6-b5f6-9e5095c314a6&quot;}">http://officecdn.microsoft.com/pr/55336b82-a18d-4dd6-b5f6-9e5095c314a6"}</a>
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Rollout Summary</td>
    <td>GET</td>
    <td>https://clients.config.office.net/rolloutProgress/v1.0/rolloutProgress/%SPGUID%/MonthlyEnterpriseChannel/%buildVersionString%/summary</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Rollout Issues</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/%buildVersionString%/Issues</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Rollout Progress</td>
    <td>GET</td>
    <td>https://clients.config.office.net/rolloutProgress/v1.0/rolloutProgress/%SPGUID%/MonthlyEnterpriseChannel/%buildVersionString%/devices?top=50</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Wave Progress</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/4/%buildVersionString%/waveprogress</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Device Rollbacks</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/MEC/%buildVersionString%/rollbackLinkedGroups</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Exclusion Windows</td>
    <td>GET</td>
    <td>https://clients.config.office.net/ServiceProfile/v1.0/ServiceProfileAggregator/%SPGUID%/servicingExclusionWindows</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
</tbody>
</table>