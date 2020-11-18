# Data Engineering and Benchmarking in Oil & Gas

## Abstract
The energy transition is just another disruption which allows Oil & Gas companies to transform and be more dynamic. Becoming a better, efficient, and responsible energy company in a carbon-intensive business has become an imperative and competitive advantage. Data is a key enabler of of this transformation. This op-ed aims to guide data engineers and IT solution architects to develop benchmarking solutions that harness the power of data and effectively democratize their consumption.

## Background
Businesses measure their performance. You cannot improve what you cannot measure. The theme today for the oil majors can be summed up in four words:
- Higher returns
- Lower carbon

From operating costs, development cycle time, resource inventory, and fugitive emissions, the energy industry has collected a ton of data related to these metrics. However, the challenge has always been publishing & consuming data to make informed decisions. The accompanying data operations (data ops) activities such as collecting, inspecting, analyzing, integrating, applying Machine Learning, and serving the data all add up to clamor for an efficient data pipeline. 

## Solution Architecture
My proposed solution architecture and data engineering pipeline ingests data in any format and structure. Data is then delivered to consumers as data products - marked as *General Availability* and *Public Preview* accordingly - that can be integrated in *any* platform and in any manner (velocity, volume, value, veracity, variety).


## Important Technical notes
- Normalized relational databases are too rigid to scale to the requirements of enormous datasets.
- Making your data products semi-structured or unstructured is an advantage.
- One row is one record. Columns denote attributes. Combination of attributes facilitate key-value pairing.
- Make your transformations dynamic i.e. your logic and transform codes have to be agnostic and portable to any platform.
- Leverage cloud resources whenever possible in order to effectively scale when warranted.
- Utilize a Master Domain Model reference from within your transformations to avoid hard-coding parameters from within sub-queries.


## Solution Architecture and Data Engineering Diagram
