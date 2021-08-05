# dvc-test

Add some data and add S3 storage
```shell
# this command will create .dvc files for every data file.
# they will be commited and tracked by Git
dvc add data/*

# this adds S3 storage. Subsequent dvc push will copy data to S3
dvc remote add -d storage s3://zzz-dvc-test/dvc-test/

# after modifying data do:
dvc commit
git commit ...

# push data files to S3 storage
dvc push
git push

# get artefact of specific commit
dvc get "git@github.com:mateuszboryn/dvc-test.git" --rev 5093d48813bffd7a22673a23f56ae9437051f2d1 data/winequality-red.csv
```


