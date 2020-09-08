## Build

```
docker build -t okassov/aws-glue-dev:ec2 .
```

## For using jupyter

```
docker run -p8888:8888 --restart=always -d okassov/aws-glue-dev-ec2 jupyter
```

## For using spark shell

```
docker run -ti -rm okassov/aws-glue-dev-ec2 pyspark
```

If you run on EC2 Instance use instance profile with permission for aws-glue

If you run localy mount your ~/.aws folder with AccessKey and SecretKey to /root/.aws


