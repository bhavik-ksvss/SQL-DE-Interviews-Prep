
---

# 📄 **File 2: 02_Find_Customer_Referee.md**

```markdown
# Find Customer Referee

Link: https://leetcode.com/problems/find-customer-referee/

## Pattern
NULL handling + filtering

## Approach 1 (Recommended)
```sql
SELECT name
FROM Customer
WHERE referee_id <> 2
   OR referee_id IS NULL;

Approach 2 (DW style)
SELECT name
FROM Customer
WHERE COALESCE(referee_id, -1) <> 2;
Approach 3 (Not preferred)
SELECT name
FROM customer
WHERE referee_id IS NULL
   OR referee_id IN (
       SELECT id FROM customer WHERE id <> 2
   );
Interview Answer

Handle NULL explicitly because NULL comparisons return UNKNOWN.

Follow-ups
Count customers without referee
Join with referee details
Mistakes
Missing NULL condition
Using = NULL
Overcomplicating with subquery
Learning

Always ask: what happens to NULL?