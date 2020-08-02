# AWS data pipeline exporter
Use AWS CloudFormation template to deploy AWS resources to launch a data pipeline
scheduling job to export records from DynamoDB to S3 bucket periodically.


## Estiamte RCU pricing
RCU (req/s) = total items / seconds

Assume you have 100w items and you wish to dump completely in 1 hour,

RCU = 1000000 / (60 * 60) = 277.778 ~= 278 (req/s)

price = 278 * 60 * 60 * 0.0001484 = 148.5 (USD per month)
