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


For using Jupyter generate password hash and use WEB_PASSWORD_HASH env

## Password Generating for Jupyter

1. Run jupyter docker
2. Create notebook and paste

```
from IPython.lib import passwd
password = passwd("your_password")
```

3. Run code and get sha1 hash

4. Use this hash in Dockerfile for local dev-endpoint and build new image


