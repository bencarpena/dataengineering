### Release notes:
>- This wiki contains the published Benchmarking Data Products
>- **General Availability (GA)**: These are data products that are production ready and are published in the **Benchmarking Master View**
>- **Public Preview**: These are data products that are still undergoing validations with their schema and structure resembling production state.
>- **Data** is a valuable asset and when collected, processed, and analyzed properly, turns into a wealth of information that help shape and guide critical business decisions 


<br />

# Benchmarking Metrics Master & Reference Views

<table>
  <tbody>
    <tr>
      <th ><b>Description</b></th>
      <th><b>Data Product(s)</b></th>
    </tr>
    <tr>
      <td><b>Benchmarking Master View </b> - contains all metrics that are in General Availability <br /><br /><b>Status</b> : GA
</td>
      <td>
        <ul>
          <li><b>dbo.vw_pr_ds5001_BenchmarkingMetrics</b></li>

<li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2174587" target="_blank">Usage details and query statements</a></li>
        </ul>
     </td>
    </tr>
  <tr>
      <td><b>Benchmarking Reference View </b> - contains all metrics that are in General Availability & Public Preview <br /><br /><b>Status</b> : In Development
</td>
      <td>
        <ul>
          <li><b>dbo.vw_rf_ds5001_BenchmarkingMetrics</b></li>

<li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2174609" target="_blank">Usage details and query statements</a></li>
        </ul>
     </td>
    </tr>
</table>
<br />

# Benchmarking Data Foundation Data Products per Metric

<table>
  <tbody>
    <tr>
      <th ><b>High-impact metric</b></th>
      <th><b>Data Product(s)</b></th>
    </tr>
    <tr>
      <td><b>COFDA</b> - Cost of Finding, Development and Acquisitions <br /><br /><b>Status</b> : GA

</td>
      <td>
        <ul>
          <li>dbo.vw_pr_ds1001_COFDA</li>
          <li>dbo.vw_pr_ds1001_COFDA_COFDAPerCountry</li>
<li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/1936027" target="_blank">Sample queries & technical notes</a></li>
        </ul>
     </td>
    </tr>
    <tr>
      <td><b>Resource Inventory</b> <br /><br /> <b>Status</b> : GA</td>
      <td>
      <ul>
      <li>restricted.vw_pr_ds1201_ResourceInventory_Reserves</li>
<li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2104783" target="_blank">Sample queries & technical notes</a></li>
      </ul>
     </td>
    </tr>
    <tr>
      <td><b>Utilization</b><br /><br /> <b>Status</b> : Public Preview</td>
      <td>
     <ul>
     <li>dbo.vw_pr_ds1102_Utilization</li>
     <li>dbo.vw_pr_ds1102_Utilization_SMPC</li>
     <li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2034607" target="_blank">Sample queries & technical notes</a></li>
     </ul>
   </td>
    </tr>
    <tr>
      <td>
        <b>Realized Price</b><br /><br /> <b>Status</b> : Public Preview
      </td>
      <td>
      <ul>
          <li>dbo.vw_pr_ds1103_RealizedPrice_Monthly</li>
          <li>dbo.vw_pr_ds1103_RealizedPrice_SalesPrice</li>
<li>dbo.vw_pr_ds1103_RealizedPrice_TransportationCost</li>
 <li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/1970502" target="_blank">Sample queries & technical notes</a></li>
        </ul>
     </td>
    </tr>
 <tr>
      <td>
        <b>Unit Operating Cost</b><br /><br /> <b>Status</b> : Public Preview
      </td>
      <td>
      <ul>
          <li>dbo.vw_pr_ds1101_UnitOperatingCost_Monthly</li>
          <li>dbo.vw_pr_ds1101_UnitOperatingCost_Detail_Monthly</li>
<li>dbo.vw_pr_ds1104_JDE_UnitOperatingCost</li>
<li>dbo.vw_pr_ds1103_RealizedPrice_TransportationCost</li>
 <li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/1989034" target="_blank">Sample queries & technical notes</a></li>
        </ul>
     </td>
    </tr>
  </tbody>
</table>

# Other Data Products

<table>
  <tbody>
    <tr>
      <th ><b>Data Series</b></th>
      <th><b>Data Product(s)</b></th>
    </tr>
    <tr>
      <td><b>ds0000</b> - Custom system metrics & logs <br /><br /><b>Status</b> : GA

</td>
      <td>
        <ul>
          <li><b>dbo.vw_pr_ds0000_MasterDomainModel</b> - master data model view. Query notes <a href='https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2174595' target=_blank>here</a>.</li>
          <li><b>dbo.vw_pr_ds0000_MetricsTabulation</b> - contains index and running status of all Benchmarking metrics. Query notes <a href='https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2174599' target=_blank>here</a>.</li>
          <li>dbo.vw_pr_ds0000_Ingested_Index</li>
          <li>dbo.vw_pr_ds0000_Metrics_DemoDay_Report</li>
<li>dbo.t_pr_ds0000_Syslogs</li>
        </ul>
    <tr>
      <td><b>Revenue</b> <br /><br /> <b>Status</b> : Public Preview</td>
      <td>
      <ul>
      <li>dbo.vw_pr_ds1101_RevenueTotalnet</li>
<li><a href="https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/1947733" target="_blank">Sample queries & technical notes</a></li>
      </ul>
     </td>
    </tr>
    
  </tbody>
</table>