## k8s data feed

Export a list of instances with:

```bash
node run.js [aws|gcp|azure|all]
```

#### generate the input files
````bash
aws ec2 describe-instance-types --instance-types > aws.json
````
````bash
gcloud compute machine-types list  --filter="zone:us-east1-b" > gcp.txt
````
````bash
az vm list-sizes --location eastus > az.json
````
#### generate the pricing files
````bash
wget https://pricing.us-east-1.amazonaws.com/offers/v1.0/aws/AmazonEC2/current/us-east-1/index.json -O aws-pricing.json
````
````bash
wget https://cloudpricingcalculator.appspot.com/static/data/pricelist.json -O gcp-pricing.json
````
````bash
export json from https://azureprice.net/
````
