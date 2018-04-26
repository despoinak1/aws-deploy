# Deploy on AWS
This is a python example to be deployed on aws. Code build will be used which will store the files to S3

# How to use

An AWS code build job is created so that any time there is a new commit in the branches specified,
the tests will be run and the application files will be stored in S3 path.
If you manually run only the code build job the rest will be stored in S3 path "sms-artifactory/app-name/artifacts/v1.3.0" as long as the following are specified  from the advanced options of the new build:
```
Name: v1.3.0
Path: app-name/artifacts/
Bucket name: sms-artifactory
```

The buildspec.yml will need to be in your application path unless you manually copy its contents to the relevant field while creating the code build job.
