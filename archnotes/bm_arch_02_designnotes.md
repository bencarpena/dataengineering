# Optimized Performance starts with Design & Architecture

## Common Relational Structure : Effects on Queries 
- **Structure**: Normalized, indexed and structured
- Sample query below returns _67,182_ records for a month's worth of data for 1 SBU (Strategic Business Unit). Elapsed time of **336,138 ms** and CPU time of **78,218 ms**
- Clearly not optimized for consumption

```
SELECT 
            sod.CostElementKey,
            sod.CostCenterkey,
            scc.CostCenter,
            SUM(sod.Amount) as Sum_OpexNonMaint,
            scc.StrategicBusinessUnit,
			sod.CalendarDateKey,
			sce.CostCategory,
			sce.CostSubcategory

        From t_rf_ds1101_CUPR_SAPOpexDetail sod

            Inner Join t_rf_ds1101_CUPR_SAPCostElement sce
            On sod.CostElementKey = sce.CostElementKey

            Inner Join t_rf_ds1101_CUPR_SAPCostCenter scc
            On scc.CostCenterKey = sod.CostCenterKey

        Where
            sce.MaintenanceRelated = 'Non-Maint.'
			
			And scc.GNAFlag <> 'General and Admin'

			
			And sce.CostCategory = 'Production Operations'
			And  scc.StrategicBusinessUnit = 'SJV'
			And LEFT(sod.CalendarDateKey, 4) = '2019'

        Group by 	
            sod.CostElementKey, 
            sod.CostCenterkey, 
            scc.StrategicBusinessUnit,
            scc.CostCenter,
			sod.CalendarDateKey,
			sce.CostCategory,
			sce.CostSubcategory
```

## Benchmarking Data Foundation Design approach & Structure : Effects on Queries
- **Structure**: No normalization; indexed
- Sample query returns _67,182 records_ with an elapsed time of **4,875 ms** and CPU time of **4,220 ms**


```
SELECT  * From t_rf_ds1101_UnitOperatingCost_UnitProdOpex_OpexNonMaintnet
Where CostCategory = 'Production Operations'
And SBU  = 'SJV'
And LEFT(CalendarDateKey, 4) = '2019'
```

## Benchmarking Data Foundation Design approach & Structure : t_pr_ds5001_BenchmarkingMetrics
- **Structure**: Semi-structured; key-value pairs; optimized for consumption
- Sample query returns _814 records_ with an elapsed time of **5 ms** and CPU time of **0 ms**


```
SELECT * From dbo.t_pr_ds5001_BenchmarkingMetrics
Where	SBU = 'SJV'
		And METRIC_STATUS = 'General Availability'
```



