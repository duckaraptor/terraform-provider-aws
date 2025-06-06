---
subcategory: "Lambda"
layout: "aws"
page_title: "AWS: aws_lambda_function"
description: |-
  Provides a Lambda Function data source.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_lambda_function

Provides information about a Lambda Function.

## Example Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { VariableType, TerraformVariable, TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsLambdaFunction } from "./.gen/providers/aws/data-aws-lambda-function";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    /*Terraform Variables are not always the best fit for getting inputs in the context of Terraform CDK.
    You can read more about this at https://cdk.tf/variables*/
    const functionName = new TerraformVariable(this, "function_name", {
      type: VariableType.STRING,
    });
    new DataAwsLambdaFunction(this, "existing", {
      functionName: functionName.stringValue,
    });
  }
}

```

## Argument Reference

This data source supports the following arguments:

* `functionName` - (Required) Name of the lambda function.
* `qualifier` - (Optional) Alias name or version number of the lambda functionE.g., `$LATEST`, `my-alias`, or `1`. When not included: the data source resolves to the most recent published version; if no published version exists: it resolves to the most recent unpublished version.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `architectures` - Instruction set architecture for the Lambda function.
* `arn` - Unqualified (no `:QUALIFIER` or `:VERSION` suffix) ARN identifying your Lambda Function. See also `qualifiedArn`.
* `codeSha256` - Base64-encoded representation of raw SHA-256 sum of the zip file.
* `codeSigningConfigArn` - ARN for a Code Signing Configuration.
* `deadLetterConfig` - Configure the function's *dead letter queue*.
* `description` - Description of what your Lambda Function does.
* `environment` - Lambda environment's configuration settings.
* `ephemeralStorage` - Amount of Ephemeral storage(`/tmp`) allocated for the Lambda Function.
* `fileSystemConfig` - Connection settings for an Amazon EFS file system.
* `handler` - Function entrypoint in your code.
* `imageUri` - URI of the container image.
* `invokeArn` - ARN to be used for invoking Lambda Function from API Gateway. **NOTE:** Starting with `v4.51.0` of the provider, this will *not* include the qualifier.
* `kmsKeyArn` - ARN for the KMS encryption key.
* `lastModified` - Date this resource was last modified.
* `layers` - List of Lambda Layer ARNs attached to your Lambda Function.
* `loggingConfig` - Advanced logging settings.
* `memorySize` - Amount of memory in MB your Lambda Function can use at runtime.
* `qualifiedArn` - Qualified (`:QUALIFIER` or `:VERSION` suffix) ARN identifying your Lambda Function. See also `arn`.
* `qualifiedInvokeArn` - Qualified (`:QUALIFIER` or `:VERSION` suffix) ARN to be used for invoking Lambda Function from API Gateway. See also `invokeArn`.
* `reservedConcurrentExecutions` - The amount of reserved concurrent executions for this lambda function or `-1` if unreserved.
* `role` - IAM role attached to the Lambda Function.
* `runtime` - Runtime environment for the Lambda function.
* `signingJobArn` - ARN of a signing job.
* `signingProfileVersionArn` - The ARN for a signing profile version.
* `sourceCodeHash` - (**Deprecated** use `codeSha256` instead) Base64-encoded representation of raw SHA-256 sum of the zip file.
* `sourceCodeSize` - Size in bytes of the function .zip file.
* `timeout` - Function execution time at which Lambda should terminate the function.
* `tracingConfig` - Tracing settings of the function.
* `version` - The version of the Lambda function returned. If `qualifier` is not set, this will resolve to the most recent published version. If no published version of the function exists, `version` will resolve to `$LATEST`.
* `vpcConfig` - VPC configuration associated with your Lambda function.

<!-- cache-key: cdktf-0.20.8 input-71534c0bfa9b2f3fbec6fbdea8297e44a5fc241d5d79c669e54ca36dac584425 -->