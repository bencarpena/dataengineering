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





