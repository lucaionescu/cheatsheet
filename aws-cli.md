### sts

```bash
# Get the current user
aws sts get-caller-identity
```

### sagemaker

```bash
# Invoke Sagemaker endpoint
aws sagemaker-runtime invoke-endpoint --endpoint-name ENDPOINT_NAME --body '{"foo": "bar"}' prediction.csv  --cli-binary-format raw-in-base64-out --content-type application/json
```

### cloudwatch

```bash
# Get CloudWatch logs for log group and stream
aws logs get-log-events --log-group-name LOG_GROUP_NAME --log-stream-name LOG_STREAM_NAME --output text > output.log
```
