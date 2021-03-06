# Amazon DynamoDB Table Projection<a name="aws-properties-dynamodb-projectionobject"></a>

Attributes that are copied \(projected\) from the source table into the index\. These attributes are additions to the primary key attributes and index key attributes, which are automatically projected\.

Projection is a property of the  and  property types\.

## Syntax<a name="w3ab2c21c14d537b7"></a>

### JSON<a name="aws-properties-dynamodb-projectionobject-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-projectionobj-nonkeyatt)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-projectionobj-projtype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-projectionobject-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-projectionobj-nonkeyatt):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-projectionobj-projtype): String
```

## Properties<a name="w3ab2c21c14d537b9"></a>

For more information about each property, including constraints, see [ Projection](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_Projection.html) in the *Amazon DynamoDB API Reference*\.

`NonKeyAttributes`  
The non\-key attribute names that are projected into the index\.  
For local secondary indexes, the total count of `NonKeyAttributes` summed across all of the local secondary indexes must not exceed 20\. If you project the same attribute into two different indexes, this counts as two distinct attributes in determining the total\. This limit does not apply for secondary indexes with a ProjectionType of `KEYS_ONLY` or `ALL`\.  
*Required: *No  
*Type*: List of String values

`ProjectionType`  
The set of attributes that are projected into the index:    
`KEYS_ONLY`  
Only the index and primary keys are projected into the index\.  
`INCLUDE`  
Only the specified table attributes are projected into the index\. The list of projected attributes are in `NonKeyAttributes`\.  
`ALL`  
All of the table attributes are projected into the index\.
*Required: *Yes  
*Type*: String