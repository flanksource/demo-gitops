Port-forward localstack pod and run:

```
terraform apply
```

Upload terraform statefile:
```
aws s3 ls s3://example-bucket-terraform --endpoint-url=http://localhost:4566

aws s3 cp terraform.tfstate s3://example-bucket-terraform/terraform.tfstate --endpoint-url=http://localhost:4566
```
