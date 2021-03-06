# Amazon S3 Bucket Destination<a name="aws-properties-s3-bucket-destination"></a>

<a name="aws-properties-s3-bucket-destination-description"></a>The `Destination` property type specifies information about where to publish analysis or configuration results for an Amazon S3 bucket\.

<a name="aws-properties-s3-bucket-destination-inheritance"></a> `Destination` is a property of the [Amazon S3 Bucket DataExport](aws-properties-s3-bucket-dataexport.md) and [Amazon S3 Bucket InventoryConfiguration](aws-properties-s3-bucket-inventoryconfiguration.md) property types\. 

## Syntax<a name="aws-properties-s3-bucket-destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-destination-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-bucketaccountid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-bucketarn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-format)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-prefix)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-destination-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-bucketaccountid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-bucketarn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-format): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-destination-prefix): String
```

## Properties<a name="aws-properties-s3-bucket-destination-properties"></a>

`BucketAccountId`  
The ID of the account that owns the destination bucket where the analytics is published\.   
Although optional, we recommend that the value be set to prevent problems if the destination bucket ownership changes\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`BucketArn`  
The Amazon Resource Name \(ARN\) of the bucket where analytics results are published\. This destination bucket must be in the same region as the bucket used for the analytics or inventory configuration\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Format`  
Specifies the output format of the analytics or inventory results\. Currently, Amazon S3 supports the comma\-separated value \(CSV\) format\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Prefix`  
The prefix that is prepended to all analytics results\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 