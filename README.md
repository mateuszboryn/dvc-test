# dvc-test

Add some data and add S3 storage
```shell
# this command will create .dvc files for every data file.
# they will be commited and tracked by Git
dvc add data/*

# this adds S3 storage. Subsequent dvc push will copy data to S3
dvc remote add -d storage s3://zzz-dvc-test/dvc-test/

# 
dvc commit

# push data files to S3 storage
dvc push
```


