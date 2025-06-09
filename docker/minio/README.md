To start:
```docker-compose up```

If MinIO Client (_mc_) is installed:
 ```mc alias set localminio http://localhost:9000 <admin_name> <admin_password>```

To create a bucket: 
``` mc mb localminio/<bucket_name>```

To list buckets:
```mc ls localminio```
