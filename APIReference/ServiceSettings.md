# Service Settings

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
  <tr><tr>
    <td>Tenant Features</td>
    <td>GET</td>
    <td>https://clients.config.office.net/onboarding/odata/v1.0/FeatureData</td>
    <td>
<pre lang="json">
{
  "featureName": "Inventory",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "LearningConsentB",
  "learningConsentAgreementVersion": "v1",
  "eligibilityRequirement": "AllOfficeAppsServicePlans"
},
{
  "featureName": "ServicingProfile",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "LearningConsentB",
  "learningConsentAgreementVersion": "v1",
  "eligibilityRequirement": "AllOfficeAppsServicePlans"
},
{
  "featureName": "SecurityCurrency",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "LearningConsentB",
  "learningConsentAgreementVersion": "v1",
  "eligibilityRequirement": "AllOfficeAppsServicePlans"
},
{
  "featureName": "OneDrive",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "NoRestrictions"
},
{
  "featureName": "AppHealth",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "LearningConsentB",
  "learningConsentAgreementVersion": "v1",
  "eligibilityRequirement": "AllOfficeAppsServicePlans"
},
{
  "featureName": "TenantAssociationKey",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "NoRestrictions"
},
{
  "featureName": "Settings",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "NoRestrictions"
},
{
  "featureName": "PolicyManagement",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "NoRestrictions"
},
{
  "featureName": "SecurityPolicyAdvisor",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "EnterpriseAppsServicePlans"
},
{
  "featureName": "DeviceConfiguration",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "NoRestrictions"
},
{
  "featureName": "ServiceHealth",
  "featureRing": "GA",
  "featureRingAgreementVersion": "None",
  "learningConsent": "None",
  "learningConsentAgreementVersion": "None",
  "eligibilityRequirement": "NoRestrictions"
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Feature Provision</td>
    <td>GET</td>
    <td>https://clients.config.office.net/onboarding/odata/v1.0/FeatureProvisiondata</td>
    <td>
<pre lang="json">
{
  "featureName": "OCPSWin32Migration",
  "featureProvisionStatus": "Unknown",
  "featureMigrationStatus": "SubstrateOnlyTenant"
},
{
  "featureName": "Inventory",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "TenantAssociationKey",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "ServicingProfile",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "SecurityCurrency",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "OneDrive",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "AppHealth",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "Settings",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "PolicyManagement",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "SecurityPolicyAdvisor",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "DeviceConfiguration",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
},
{
  "featureName": "ServiceHealth",
  "featureProvisionStatus": "Provisioned",
  "featureMigrationStatus": "NotStarted"
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Feature Elibility</td>
    <td>GET</td>
    <td>https://clients.config.office.net/onboarding/odata/v1.0/EligibilityRecord</td>
    <td>
<pre lang="json">
{
  "id": "00000000-0000-0000-0000-000000000000",
  "eligibilities": [
  "AllOfficeAppsServicePlans",
  "EnterpriseAppsServicePlans"
  ]
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Agreement Data</td>
    <td>GET</td>
    <td>https://clients.config.office.net/onboarding/odata/v1.0/Agreementdata</td>
    <td>
<pre lang="json">
{
  "featureRing": "None",
  "learningConsent": "LearningConsentB",
  "version": "v1",
  "acceptDateTime": "2022-08-26T16:42:17.7827778Z",
  "isAccepted": true
}
</pre>
    </td>
  </tr>
  <tr>
    <td>Service Health</td>
    <td>GET</td>
    <td>https://clients.config.office.net/appConfig/v1.0/ServiceHealth</td>
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