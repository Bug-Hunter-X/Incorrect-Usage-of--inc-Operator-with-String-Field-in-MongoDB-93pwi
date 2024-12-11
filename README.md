# Incorrect Usage of $inc Operator with String Field in MongoDB
This example demonstrates an uncommon error in MongoDB where the `$inc` operator is used incorrectly with a string field.  The `$inc` operator is designed to increment numeric values, and using it with a string will result in unexpected behavior or an error.

**Problem:** The provided code attempts to increment a string field using `$inc`. This is invalid and will not produce the desired result. It may either throw an error or silently fail depending on the MongoDB version and settings.

**Solution:** To increment a numerical value in a MongoDB document, ensure the field is of a numeric type (int, long, double) and use the `$inc` operator correctly.  If the field is a string and needs to be updated numerically, you must first convert it to a number and then perform the increment. 