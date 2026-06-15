# Dataset Management

*Review dataset schemas, download templates, and upload your data*

## Dataset management overview

Demand forecasting is DeepFlow's core capability, and its accuracy depends heavily on input data quality. The Dataset Management screen lets you review schemas and, when needed, upload data directly.

## Reviewing the dataset list

![Dataset list](/images/dataset/01.png)

When your team uploads its own data, you use the Dataset Management screen. The Impactive AI team sets up each dataset according to the defined schema.

## Inspecting the schema and downloading a template

Each dataset's detail page explains what every column means, the required format, and which columns are required versus optional.

### Download the template

Click **Download template** to get the data-entry template.

### Enter data

Populate the template according to the required format.

> **Note:** If you need to change the defined schema, please contact us.

## Uploading data

### Open the upload screen

There are two ways to get there:
- From the dataset list, click into upload directly
- From a dataset's detail page, click **Upload data**

### Upload your file

Drag and drop or pick the file you want to upload.

> **Note:** Only `csv` and `zip` files are supported.

### Wait for validation

DeepFlow validates the file after upload. If errors are reported, fix them and re-upload.

> **Warning:** **Common errors**
>
> - `dt` (date): Use the `yyyy-mm-dd` format (for example, `2025-01-01`).
> - `v` (shipment volume): Enter the value without commas. (`9000` ✅ / `9,000` ❌)
> - `post_inv` (ending inventory): Enter the value without commas. (`9000` ✅ / `9,000` ❌)

### Confirm the partitions

Check the row count for each partition in your file and select the partitions you actually want to commit. For partitions that already exist, you can see the currently registered row count.

### Finalize the upload

Click **Upload data** to commit.

> **Note:** Rows in existing partitions are overwritten.

After the upload completes, the dataset detail page reflects the new row counts per partition.
