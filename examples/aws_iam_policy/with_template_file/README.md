# IAM policy with file source example
Configuration in this directory creates IAM policy and IAM policy document by rendering `iam_policy_document.tmpl` template file with the help of `template_file` and `template_variables` variables.

This policy contains a rule that allows listing any s3 bucket.

## Usage
To run this example you have to set AWS-related environment variables, at least `AWS_PROFILE` and `AWS_DEFAULT_REGION`. After that you need to execute following commands:
```
$ terraform init
$ terraform plan
$ terraform apply
```
**Note:** this example creates resources that may cost money. So, after you have no need in these resources, run `terraform destroy` to get rid of them.

## Outputs
| Name | Description |
|------|-------------|
| iam_policy_id | Id of the newly-created IAM policy. |
| iam_policy_arn | ARN of the newly-created IAM policy. |
| iam_policy_name | Name of the newly-created IAM policy. |
| iam_policy_path | Path of the newly-created IAM policy. |
| iam_policy_document | Contents of the IAM policy document. |