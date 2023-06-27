# Apps Health

Portal Link: https://config.office.com/officeSettings/officeapphealth/overview

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
    <td>Health Onboarding</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/v2/onboarding</td>
    <td>
<pre lang="json">
{
    "provisioningStatus": 2,
    "cookingStatus": 2,
    "onboardingDate": "%DateTime%",
    "lastDataRefreshedEpochInSeconds": 1687737600,
    "dataBoundary": 1
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Windows Health Insights</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/currencyinsights?officePlatform=Windows&architecture=All</td>
    <td>
<pre lang="json">
{
    "buildsWithAdvisoriesPercentage": 0.0,
    "activeAdvisoriesDeviceCount": 0,
    "devicesOnRecommendedChannelsPercentage": 100.0,
    "devicesOnCurrentChannelPercentage": 0.0,
    "devicesOnMonthlyEnterpriseChannelPercentage": 100.0,
    "devicesNotOnLatestBuildPercentage": 50.0,
    "devicesOnUnsupportedBuildPercentage": 0.0,
    "totalDevicesCount": 2,
    "buildsWithActiveAdvisories": []
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Windows Health Alerts</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/product/alerts/current?officePlatform=Windows</td>
    <td>
<pre lang="json">
{
    "officeProductHealthAlerts":[]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Device Diagnostic Summary</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/diagnosticscoverage/devices</td>
    <td>
<pre lang="json">
{
    "deviceDiagnosticCoverages": [
        {
            "platform": "Windows",
            "officeServicingChannel": "MonthlyEnterpriseChannel",
            "monitored": 1,
            "active": 1,
            "noTelemetry": 0
        }
    ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>User Diagnostic Summary</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/diagnosticscoverage/users</td>
    <td>
<pre lang="json">
{
    "userDiagnosticCoverages": [
        {
            "platform": "Windows",
            "officeServicingChannel": "MonthlyEnterpriseChannel",
            "monitored": 1,
            "active": 1,
            "noTelemetry": 0
        }
    ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>App Metrics</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/product/metrics?officePlatform=Windows</td>
    <td>
<pre lang="json">
{
    "officeProductMetrics": [
        {
            "officeProduct": "Access",
            "monitoredSessionCount": 0,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": -1.0,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": -1,
            "performanceAlertCount": -1,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        },
        {
            "officeProduct": "Excel",
            "monitoredSessionCount": 0,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": -1.0,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": -1,
            "performanceAlertCount": -1,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        },
        {
            "officeProduct": "OneNote",
            "monitoredSessionCount": 0,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": -1.0,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": -1,
            "performanceAlertCount": -1,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        },
        {
            "officeProduct": "Outlook",
            "monitoredSessionCount": 6,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": 0.6666666666666666,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": 0,
            "performanceAlertCount": 0,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        },
        {
            "officeProduct": "PowerPoint",
            "monitoredSessionCount": 0,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": -1.0,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": -1,
            "performanceAlertCount": -1,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        },
        {
            "officeProduct": "Publisher",
            "monitoredSessionCount": 0,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": -1.0,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": -1,
            "performanceAlertCount": -1,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        },
        {
            "officeProduct": "Word",
            "monitoredSessionCount": 3,
            "monitoredDeviceCount": -1,
            "monitoredUserCount": -1,
            "usageRatio": 0.3333333333333333,
            "reliabilityScore": -1.0,
            "performanceScore": -1.0,
            "reliabilityMetricTypesWithIssues": [],
            "performanceMetricTypesWithIssues": [],
            "reliabilityAlertCount": 0,
            "performanceAlertCount": 0,
            "addInPerformanceAlertCount": 0,
            "addInReliabilityAlertCount": 0
        }
    ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Build Metrics</td>
    <td>GET</td>
    <td>https://health.insights.office.net/health/api/build/metrics?officePlatform=Windows</td>
    <td>
<pre lang="json">
{
    "officeBuildServicingChannelMetrics": [
        {
            "officeServicingChannel": "MonthlyEnterpriseChannel",
            "officeBuildMetrics": [
                {
                    "buildVersion": "16.0.16327.20324",
                    "releaseVersion": "2304",
                    "isSupported": true,
                    "isBaseline": false,
                    "isLast": true,
                    "isLatest": true,
                    "monitoredSessionCount": 6,
                    "monitoredDeviceCount": 1,
                    "reliabilityScore": -1.0,
                    "performanceScore": -1.0,
                    "reliabilityMetricTypesWithIssues": [],
                    "performanceMetricTypesWithIssues": [],
                    "reliabilityAlertCount": 0,
                    "performanceAlertCount": 0,
                    "addInPerformanceAlertCount": 0,
                    "addInReliabilityAlertCount": 0
                },
                {
                    "buildVersion": "16.0.16227.20318",
                    "releaseVersion": "2303",
                    "isSupported": true,
                    "isBaseline": true,
                    "isLast": false,
                    "isLatest": false,
                    "monitoredSessionCount": 3,
                    "monitoredDeviceCount": 1,
                    "reliabilityScore": -1.0,
                    "performanceScore": -1.0,
                    "reliabilityMetricTypesWithIssues": [],
                    "performanceMetricTypesWithIssues": [],
                    "reliabilityAlertCount": 0,
                    "performanceAlertCount": 0,
                    "addInPerformanceAlertCount": 0,
                    "addInReliabilityAlertCount": 0
                }
            ]
        }
    ]
}
</pre>
    </td>
  </tr>
</tbody>
</table>