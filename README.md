# de-zoomcamp

02-workflow-orchestration

-- 1. Within the execution for Yellow Taxi data for the year 2020 and month 12: what is the uncompressed file size (i.e. the output file yellow_tripdata_2020-12.csv of the extract task)

128.3 MB

-- 2. What is the rendered value of the variable file when the inputs taxi is set to green, year is set to 2020, and month is set to 04 during execution?

Kestra template: {{inputs.taxi}}_tripdata_{{inputs.year}}-{{inputs.month}}.csv

Inputs:
inputs.taxi = "green"
inputs.year = "2020"
inputs.month = "04"

Result: green_tripdata_2020-04.csv

-- 3. How many rows are there for the Yellow Taxi data for all CSV files in the year 2020?

select count(*)
from my_ds_zoomcamp.yellow_tripdata
where filename like '%2020%';

-- 4. How many rows are there for the Green Taxi data for all CSV files in the year 2020?

select count(*)
from my_ds_zoomcamp.green_tripdata
where filename like '%2020%';

-- 5. How many rows are there for the Yellow Taxi data for the March 2021 CSV file?

select count(*)
from my_ds_zoomcamp.yellow_tripdata_2021_03;

-- 6. How would you configure the timezone to New York in a Schedule trigger?

Add a timezone property set to America/New_York in the Schedule trigger configuration
