# OpenAPI Generator Issue

**Python generator infinite loop on recursive types**.

To reproduce:

`mvn package`

In the console output, observe stack overflow due to infinite loop:

```
	at org.openapitools.codegen.languages.AbstractPythonCodegen.toExampleValueRecursive(AbstractPythonCodegen.java:418)
	at org.openapitools.codegen.languages.AbstractPythonCodegen.toExampleValueRecursive(AbstractPythonCodegen.java:486)
	at org.openapitools.codegen.languages.AbstractPythonCodegen.toExampleValueRecursive(AbstractPythonCodegen.java:352)
	at org.openapitools.codegen.languages.AbstractPythonCodegen.toExampleValueRecursive(AbstractPythonCodegen.java:418)
```

and so on...
