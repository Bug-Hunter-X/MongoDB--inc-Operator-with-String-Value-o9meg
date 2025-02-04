# MongoDB $inc Operator with String Value

This repository demonstrates a common error when using the `$inc` operator in MongoDB updates. The error involves providing a string value instead of a numeric value for incrementing a field. 

## Bug Description
The bug occurs when using the `$inc` operator in MongoDB to increment a field, but providing the increment value as a string instead of a number. This can lead to unexpected behavior, such as the update failing or the value not being updated correctly.

## Reproduction Steps
1.  Create a MongoDB collection (e.g., `myCollection`) with a document containing a numeric field (e.g., `count`).
2.  Attempt to increment the field using `$inc` with a string value.

## Solution
Always use a numeric value with the `$inc` operator.  Strings will not be interpreted numerically and will lead to errors.
