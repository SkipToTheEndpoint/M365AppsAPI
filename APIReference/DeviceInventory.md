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
    <td>Inventory Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/Devices/GetDeviceSummary?api-version=1.1</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Device Builds Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/DevicesWithMetadata/GetOfficeBuildDeviceSummaryWithMetadata?api-version=1.1&amp;$count=true</td>
    <td>
<pre lang="json">
{
}
</pre>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>Device Channels Summary</td>
    <td>GET</td>
    <td>https://query.inventory.insights.office.net/inventory/api/DevicesWithMetadata/GetOfficeBuildChannelSummaryWithMetadata?api-version=1.1&amp;$orderby=officeBuildCount%20desc&amp;$count=true</td>
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