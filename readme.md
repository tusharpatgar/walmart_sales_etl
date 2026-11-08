# Walmart Sales Analytics — PySpark Notebook

A notebook-based data transformation exercise using PySpark and Databricks. It cleans weekly Walmart sales records, derives calendar attributes, and calculates store-level sales aggregations.

## Project contents

```text
Notebooks/
  ETL PROCESS.ipynb
datasets/
  Walmart_Sales.csv
readme.md
```

## Technology

- Python
- Apache Spark / PySpark
- Databricks notebooks
- Spark DataFrames and SQL tables

## Notebook workflow

The notebook demonstrates:

1. Defining a Spark schema for sales records.
2. Loading a source table into a Spark DataFrame.
3. Selecting and casting fields.
4. Filtering invalid or incomplete sales records.
5. Deriving year, month, week, and holiday indicators.
6. Writing a cleaned table.
7. Aggregating weekly sales by store and calendar period.

## Data

The repository includes `datasets/Walmart_Sales.csv`. The notebook currently reads a Databricks table named `walmart_sales` and later references a workspace table. Configure the required table(s) in your Databricks workspace before running the notebook, or update the notebook to read the repository CSV directly.

## Run the notebook

1. Import this repository into a Databricks workspace or open the notebook in a compatible notebook environment.
2. Ensure the source data is available as the `walmart_sales` table.
3. Review the catalog/schema references and update them for your workspace.
4. Run `Notebooks/ETL PROCESS.ipynb` from top to bottom.

This repository does not currently provide a local Spark application entry point or a fully automated deployment pipeline.

## Important implementation notes

- The notebook writes tables using overwrite mode. Confirm the target table and workspace before rerunning it.
- Validate the declared schema against the source CSV columns before using the CSV as the table source.
- The current notebook is an educational transformation workflow. Do not describe it as an incremental, idempotent production pipeline without implementing and testing those behaviors.

## Possible next improvements

- Read the committed CSV directly instead of relying on a pre-created source table.
- Parameterize catalog, schema, and table names.
- Add schema and data-quality assertions.
- Add reproducible run instructions and sample outputs.

## License

No license is currently specified. Contact the repository owner before reusing the contents.
