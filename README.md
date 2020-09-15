####Run and test function locally: 
mvn function:run

####How to push to gcp:

1. mvn package
2. Deploy to gcp (requires gcp setup) 
```
    gcloud functions deploy gcp-cloud-function \
    --entry-point org.springframework.cloud.function.adapter.gcp.GcfJarLauncher \
    --runtime java11 \
    --trigger-http \
    --source target/deploy \
    --memory 256MB
```
  where, gcp-cloud-function: is supposed to same as artifact name.

