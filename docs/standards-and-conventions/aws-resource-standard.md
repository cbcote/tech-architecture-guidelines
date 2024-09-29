# AWS Resource Naming Standards

### Key Elements

| Element       | Description                       | Examples                                    |
|---------------|-----------------------------------|---------------------------------------------|
| Resource Type | Abbreviations for resource types  | `ec2` (EC2 Instance), `s3` (S3 Bucket), `rds` (RDS Instance), `sg` (Security Group), `vpc` (VPC), `elb` (Elastic Load Balancer), `lambda` (Lambda Function), `dynamodb` (DynamoDB Table), `cloudwatch` (CloudWatch Log Group) |
| Environment   | Indicates the environment         | `prod` (Production), `dev` (Development), `test` (Testing), `stage` (Staging) |
| Region        | AWS region codes                  | `us-east-1` (N. Virginia), `us-west-2` (Oregon), `eu-west-1` (Ireland), `ap-southeast-1` (Singapore), `ap-northeast-1` (Tokyo) |
| Instance      | Unique identifier or instance number | Use a numeric value or a short identifier |

### Examples

| Resource Type       | Example Naming Convention       | Example Name         |
|---------------------|---------------------------------|----------------------|
| EC2 Instance        | `ec2-[environment]-[region]-[instance]` | `ec2-prod-us-east-1-01` |
| S3 Bucket           | `s3-[environment]-[region]-[instance]` | `s3-dev-us-west-2-01`   |
| RDS Instance        | `rds-[environment]-[region]-[instance]` | `rds-test-eu-west-1-01` |
| Security Group      | `sg-[environment]-[region]-[instance]`  | `sg-stage-ap-southeast-1-01` |
| VPC                 | `vpc-[environment]-[region]-[instance]` | `vpc-prod-ap-northeast-1-01` |
| Elastic Load Balancer | `elb-[environment]-[region]-[instance]` | `elb-dev-us-east-1-01`   |
| Lambda Function     | `lambda-[environment]-[region]-[instance]` | `lambda-test-us-west-2-01` |
| DynamoDB Table      | `dynamodb-[environment]-[region]-[instance]` | `dynamodb-stage-eu-west-1-01` |
| CloudWatch Log Group | `cloudwatch-[environment]-[region]-[instance]` | `cloudwatch-prod-ap-southeast-1-01` |

## Conclusion
Following these naming standards will help ensure consistency and clarity across all AWS resources. Make sure to adhere to these guidelines for all new resources.