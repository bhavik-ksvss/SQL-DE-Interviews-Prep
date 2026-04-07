# Recyclable and Low Fat Products

Link: https://leetcode.com/problems/recyclable-and-low-fat-products/

## Pattern
Filtering (AND condition)

## Approach
```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y'
  AND recyclable = 'Y';

Simple filter using AND to satisfy both conditions.

Follow-ups
Count such products
% of such products
Add GROUP BY if category exists
Mistakes
Using OR instead of AND
Missing one condition
Learning

Don’t overcomplicate simple filters.