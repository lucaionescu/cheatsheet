```bash
# Get the current user
aws sts get-caller-identity

# Invoke Sagemaker endpoint
aws sagemaker-runtime invoke-endpoint --endpoint-name ENDPOINT_NAME --body '{"foo": "bar"}' prediction.csv  --cli-binary-format raw-in-base64-out --content-type application/json
```
