# Amazon EMR Step HadoopJarStepConfig<a name="aws-properties-emr-step-hadoopjarstepconfig"></a>

`HadoopJarStepConfig` is a property of the [AWS::EMR::Step](aws-resource-emr-step.md) resource that specifies a JAR file and runtime settings that Amazon EMR \(Amazon EMR\) executes\.

## Syntax<a name="w3ab2c21c14e1010b5"></a>

### JSON<a name="aws-properties-emr-step-hadoopjarstepconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-args)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-jar)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-mainclass)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-stepproperties)" : [ KeyValue, ... ]
}
```

### YAML<a name="aws-properties-emr-step-hadoopjarstepconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-args):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-jar): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-mainclass): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-step-hadoopjarstepconfig-stepproperties):
  - KeyValue
```

## Properties<a name="w3ab2c21c14e1010b7"></a>

`Args`  
A list of command line arguments passed to the JAR file's main function when the function is executed\.  
*Required: *No  
*Type*: List of String values

`Jar`  
A path to the JAR file that Amazon EMR runs for the job flow step\.  
*Required: *Yes  
*Type*: String

`MainClass`  
The name of the main class in the specified JAR file\. If you don't specify a value, you must specify a main class in the JAR file's manifest file\.  
*Required: *No  
*Type*: String

`StepProperties`  
A list of Java properties that are set when the job flow step runs\. You can use these properties to pass key\-value pairs to your main function in the JAR file\.  
*Required: *No  
*Type*: List of [Amazon EMR Step KeyValue](aws-properties-emr-step-hadoopjarstepconfig-keyvalue.md)