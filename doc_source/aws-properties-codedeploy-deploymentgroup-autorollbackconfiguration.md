# AWS CodeDeploy DeploymentGroup AutoRollbackConfiguration<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration"></a>

The `AutoRollbackConfiguration` property type configures automatic rollback for an AWS CodeDeploy deployment group when a deployment doesn't complete successfully\. For more information, see [Automatic Rollbacks](http://docs.aws.amazon.com/codedeploy/latest/userguide/deployments-rollback-and-redeploy.html#deployments-rollback-and-redeploy-automatic-rollbacks) in the *AWS CodeDeploy User Guide*\.

 `AutoRollbackConfiguration` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource\. 

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-enabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-events)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-enabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration-events): 
  - String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration-properties"></a>

`Enabled`  
Indicates whether a defined automatic rollback configuration is currently enabled\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Events`  
The event type or types that trigger a rollback\. Valid values are `DEPLOYMENT_FAILURE`, `DEPLOYMENT_STOP_ON_ALARM`, or `DEPLOYMENT_STOP_ON_REQUEST`\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 