# OpenAPI Generator Issue

**Reserved words detection in JS client generator is case-insensitive**.

To reproduce:

`mvn package`

In the console output, observe multiple cases of this warning:

```
[WARNING] InstanceOf (reserved word) cannot be used as model name. Renamed to ModelInstanceOf
```

This should not occur, since `InstanceOf` is not a reserved word (while `instanceof` is).