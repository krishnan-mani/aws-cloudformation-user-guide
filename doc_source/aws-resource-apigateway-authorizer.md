# AWS::ApiGateway::Authorizer<a name="aws-resource-apigateway-authorizer"></a>

The `AWS::ApiGateway::Authorizer` resource creates an authorization layer that Amazon API Gateway \(API Gateway\) activates for methods that have authorization enabled\. API Gateway activates the authorizer when a client calls those methods\.


+ [Syntax](#aws-resource-apigateway-authorizer-syntax)
+ [Properties](#w3ab2c21c10c22b9)
+ [Return Value](#w3ab2c21c10c22c11)
+ [Examples](#w3ab2c21c10c22c13)

## Syntax<a name="aws-resource-apigateway-authorizer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-authorizer-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Authorizer",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authtype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authorizercredentials)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authorizerresultttlinseconds)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authorizeruri)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-identitysource)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-identityvalidationexpression)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-providerarns)" : [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-restapiid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-type)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-authorizer-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::Authorizer"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authtype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authorizercredentials): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authorizerresultttlinseconds): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-authorizeruri): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-identitysource): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-identityvalidationexpression): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-providerarns):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-restapiid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-apigateway-authorizer-type): String
```

## Properties<a name="w3ab2c21c10c22b9"></a>

`AuthType`  
An optional customer\-defined field that's used in Swagger imports and exports without functional impact\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`AuthorizerCredentials`  
The credentials that are required for the authorizer\. To specify an AWS Identity and Access Management \(IAM\) role that API Gateway assumes, specify the role's Amazon Resource Name \(ARN\)\. To use resource\-based permissions on the AWS Lambda \(Lambda\) function, specify null\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`AuthorizerResultTtlInSeconds`  
The time\-to\-live \(TTL\) period, in seconds, that specifies how long API Gateway caches authorizer results\. If you specify a value greater than `0`, API Gateway caches the authorizer responses\. By default, API Gateway sets this property to `300`\. The maximum value is `3600`, or 1 hour\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`AuthorizerUri`  
The authorizer's Uniform Resource Identifier \(URI\)\. If you specify `TOKEN` for the authorizer's `Type` property, specify a Lambda function URI that has the form `arn:aws:apigateway:region:lambda:path/path`\. The path usually has the form `/2015-03-31/functions/LambdaFunctionARN/invocations`\.  
*Required: *Conditional\. Specify this property for Lambda functions only\.  
*Type*: String  
*Update requires*: No interruption

`IdentitySource`  
The source of the identity in an incoming request\. If you specify `TOKEN` for the authorizer's `Type` property, specify a mapping expression\. The custom header mapping expression has the form `method.request.header.name`, where *name* is the name of a custom authorization header that clients submit as part of their requests\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`IdentityValidationExpression`  
A validation expression for the incoming identity\. If you specify `TOKEN` for the authorizer's `Type` property, specify a regular expression\. API Gateway uses the expression to attempt to match the incoming client token, and proceeds if the token matches\. If the token doesn't match, API Gateway responds with a 401 \(unauthorized request\) error code\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Name`  
The name of the authorizer\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`ProviderARNs`  
A list of the Amazon Cognito user pool Amazon Resource Names \(ARNs\) to associate with this authorizer\. For more information, see [Use Amazon Cognito Your User Pool](http://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-integrate-with-cognito.html#apigateway-enable-cognito-user-pool) in the *API Gateway Developer Guide*\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`RestApiId`  
The ID of the `RestApi` resource that API Gateway creates the authorizer in\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Type`  
The type of authorizer:  

+ For a custom authorizer that uses a Lambda function, use `TOKEN`\.

+ For an authorizer that uses Amazon Cognito user pools, use `COGNITO_USER_POOLS`\.
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10c22c11"></a>

### Ref<a name="w3ab2c21c10c22c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the authorizer's ID, such as `abcde1`\.

For more information about using the `Ref` function, see Ref\.

## Examples<a name="w3ab2c21c10c22c13"></a>

The following examples create a custom authorizer that is an AWS Lambda function\.

### JSON<a name="aws-resource-apigateway-authorizer-example.json"></a>

```
"Authorizer": {
  "Type": "AWS::ApiGateway::Authorizer",
  "Properties": {
    "AuthorizerCredentials": { "Fn::GetAtt": ["LambdaInvocationRole", "Arn"] },
    "AuthorizerResultTtlInSeconds": "300",
    "AuthorizerUri" : {"Fn::Join" : ["", [
      "arn:aws:apigateway:",
      {"Ref" : "AWS::Region"},
      ":lambda:path/2015-03-31/functions/",
      {"Fn::GetAtt" : ["LambdaAuthorizer", "Arn"]}, "/invocations"
    ]]},
    "Type": "TOKEN",
    "IdentitySource": "method.request.header.Auth",
    "Name": "DefaultAuthorizer",
    "RestApiId": {
      "Ref": "RestApi"
    }
  }
}
```

### YAML<a name="aws-resource-apigateway-authorizer-example.yaml"></a>

```
Authorizer: 
  Type: "AWS::ApiGateway::Authorizer"
  Properties: 
    AuthorizerCredentials: 
      Fn::GetAtt: 
        - "LambdaInvocationRole"
        - "Arn"
    AuthorizerResultTtlInSeconds: "300"
    AuthorizerUri: 
      Fn::Join: 
        - ""
        - 
          - "arn:aws:apigateway:"
          - Ref: "AWS::Region"
          - ":lambda:path/2015-03-31/functions/"
          - Fn::GetAtt: 
              - "LambdaAuthorizer"
              - "Arn"
          - "/invocations"
    Type: "TOKEN"
    IdentitySource: "method.request.header.Auth"
    Name: "DefaultAuthorizer"
    RestApiId: 
      Ref: "RestApi"
```