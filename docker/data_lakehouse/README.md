## Data Lakehouse

### Introduction

Data Lakehouse for this project is built upon following open-source technologies:
- **MinIO**: an S3-compatible object storage system.
- **Dremio**: SQL-based query engine. Executes queries directly on files stored in MinIO.
- **Nessie**: git-like catalog for data lakehouses. Allows using branches for data in MinIO to not affect productive data while conducting experiments. If experiments is deemed successful, data can be easily merge to the main branch.

Idea is to leverage these technologies with Apache Iceberg table format. General introduction can be found [here](https://www.dremio.com/blog/intro-to-dremio-nessie-and-apache-iceberg-on-your-laptop/#h-setting-up-dremionessieminio). 

### Local Start
Create .env file with the same structure as example.env.

To start all the necessary containers, please run: ```make up```.

If MinIO Client (_mc_) is installed:
 ```mc alias set localminio http://localhost:9000 <admin_name> <admin_password>```

To create a bucket: 
``` mc mb localminio/<bucket_name>```

To list buckets:
```mc ls localminio```

MinIO Web UI can be accessed at http://localhost:9001/. Dremio can be accessed at http://localhost:9047/

## Documentation 

[IN PROGRESS]

At the moment, we parse only news and stocks info for top-200 German companies. In MinIO they can be viewed:

- news: http://localhost:9001/browser/news
- stocks info: http://localhost:9001/browser/stock-data

Data is ingested in these according to the data flows defined [there](../airflow/README.md).
