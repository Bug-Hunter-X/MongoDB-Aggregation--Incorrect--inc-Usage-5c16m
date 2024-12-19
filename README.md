# MongoDB Aggregation Pipeline Bug: Incorrect $inc Usage

This repository demonstrates a common error when using the `$inc` operator within the `$project` stage of a MongoDB aggregation pipeline.  The `$inc` operator is intended for incrementing numeric fields, but in the example, it's used incorrectly with an array, leading to unexpected behavior.

## Bug Description
The bug lies in the incorrect application of the `$inc` operator within the `$project` stage.  The `$inc` operator expects a numeric field to increment and not an array or string. This error can lead to unexpected results or pipeline failures depending on the specific MongoDB version.

## Solution
The correct approach involves creating a new field and directly adding the value. The solution provided demonstrates the appropriate use of the `$add` operator to achieve the desired result.