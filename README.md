This is an humble attempt to map what permissions are required for different sdk calls.

All variables like `<VARIABLE>` are templated and need to be replaced with actual values.

| Service | [boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) | Action | Resource template example |
| - | - | - | - |
| ApiGateway | `create_api_key` | `apigateway:POST` | `arn:aws:apigateway:<REGION>::/apikeys` |
| ApiGateway | `create_usage_plan_key` | `apigateway:POST` | `arn:aws:apigateway:<REGION>::/usageplans/<USAGE_PLAN_ID>/keys` |
| ApiGateway | `delete_usage_plan_key` | `apigateway:DELETE` | ` arn:aws:apigateway:<REGION>::/usageplans/<USAGE_PLAN_ID>/keys/<KEY_ID>` |
| ApiGateway | `get_account` | `apigateway:GET` | `arn:aws:apigateway:<REGION>::/account` |
| ApiGateway | `get_usage_plan` | `apigateway:GET` | `arn:aws:apigateway:<REGION>::/usageplans/<USAGE_PLAN_ID>` |
| SecretsManager | `get_secret_value` | `secretsmanager:DescribeSecret` `secretsmanager:GetSecretValue` | `arn:aws:secretsmanager:<REGION>:<ACCOUNT>:secret:` |

