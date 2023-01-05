# ETL-Project-on-Youtube-Trending-Data-in-AWS

# Data Source:

This dataset is available on Kaggle.com and is a daily record of the top trending YouTube videos.This dataset includes several months of data on daily trending YouTube videos. Data is included for the US, GB, DE, CA, and FR regions (USA, Great Britain, Germany, Canada, and France, respectively), with up to 200 listed trending videos per day. Now includes data from RU, MX, KR, JP and IN regions (Russia, Mexico, South Korea, Japan and India respectively) over the same time period. Each region’s data is in a separate csv file. Data includes the video title, channel title, publish time, tags, views, likes and dislikes, description, and comment count. The data also includes a category_id field, which varies between regions. To retrieve the categories for a specific video, find it in the associated JSON. One such file is included for each of the regions in the dataset.

# Proposed Transformation:

Combine data of different regions (different csv) into one single table. Clean-up the table to include the required columns. Use the associated JSON to map the category for each region into the combined table. Any other data clean-up and preparation as required.

# The Workflow

The raw data is downloaded and put into the s3 buckets. And the json file was needde to be processed. That was done with Lambda function. The csv files are fine. Nothing to do with it. And I created the Glue catelogs for both the files. And using pyspark in glue I combined them and created the final data for analytics. Then I queried the data with Athena.

For demonstration purpose I've done this project in Jupyter Notebook using boto3.

![YT Data ETL in AWS](https://user-images.githubusercontent.com/104122875/210777920-8d563418-3eca-4b3a-b118-554497d9a41b.jpeg)
