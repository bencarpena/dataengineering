# Benchmarking Design and Structure

- Optimized for consumption
- Modern data warehouse - no rigid table design and entity relationships can easily be customized
- Employs Master Domain Model design pattern which lessens query cost and operational overhead. Further notes on [Master Domain Model here](https://docs.aws.amazon.com/AmazonSimpleDB/latest/DeveloperGuide/DataModel.html).
- Optimized for Integration + Plug and Play
- Naming convention cardinal rule : Must help the data engineer, analyst or audience to recognize what object they are looking at just by the naming convention; column names are highly descriptive

## Important Technical notes
- Normalized relational databases are too rigid to scale to the requirements of enormous datasets.
- Making your data products semi-structured or unstructured is an advantage.
- Master Domain Model Approach: One row is one record. Columns denote attributes. Combination of attributes facilitate key-value pairing.
- Utilize a Master Domain Model reference from within your transformations to avoid hard-coding parameters from within sub-queries.
- Make your transformations dynamic i.e. your logic and transform codes have to be agnostic and portable to any platform.
- Leverage cloud resources whenever possible in order to effectively scale when warranted.
- Data lake and Data Warehouse = Lake House. This is a key enabler when implemented right.

# The Benchmarking Products

## t_pr_ds5001_BenchmarkingMetrics
- Contains all processed metrics
- Data here to be fed into the data lake /produced/Finance/LeadingPerformance/ in **parquet** format
- "Distilled" and derived figures are stored here in a semi-structured format for flexibility and agility
- Low cost on backend query
- Semi-structured with _key-value pairing_ architecture
- Allows for granular and fit-for-purpose queries by other data consumers

## vw_pr_ds5001_BenchmarkingMetrics
- Renders the metrics that are in "General Availability" from the t_pr_ds5001_BenchmarkingMetrics table in a ready-to-consume format
- Data here to be fed into the data lake /produced/Finance/LeadingPerformance/


## vw_rf_ds5001_BenchmarkingMetrics
- Renders the metrics that are in "Public Preview" from the t_pr_ds5001_BenchmarkingMetrics table in a ready-to-consume format

## vw_pr_ds0000_MasterDomainModel
- Organizes benchmarking data into domains
- Helps organize t_pr_ds5001_BenchmarkingMetrics into a more consumable format
- Data here to be fed into the data lake /produced/Finance/LeadingPerformance/ in **parquet** format
- Each row represents a **record**
- Each column represents an **attribute**
- Each cell houses corresponding **values**


### Standard database table column names 
These columns are consistent all across the database tables:
1. **RECID** - Record ID; 36-character GUID; unique identifier for each record
2. **AUD_ID** - Audit ID; specifies who executed DML on the records
3. **AUD_CD** - Audit code

| Code | Meaning |
|--|--|
| 2 | Inserted; added; newly created  |
| 3 | Updated; modified  |
| 4 | Logically deleted; do _not_ include records with AUD_CD = 4 on your queries  |

4. **AUD_DT** - Audit Date; when was the record changed (insert, updated, deleted)





#### Further reads:
- go.chevron.com/benchmarking
- go.chevron.com/benchmarkingmetrics
- go.chevron.com/benchmarkingarchitecture
- go.chevron.com/benchmarkingdataproducts (legos + main product)
- Upcoming data engineering iterations & features outlined [here](https://dev.azure.com/chevron/LeadingPerformance/_workitems/edit/2184814)





