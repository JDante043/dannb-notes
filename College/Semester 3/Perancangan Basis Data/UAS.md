Read [[College/Semester 3/Perancangan Basis Data/UAS|the UTS summary]]; this appends it.

# Subqueries
Subqueries are, like the name suggests, secondary queries used in a full query.

Say we have a scenario where we have `WORKER`, `DIVISION`, and `BRANCH`tables. A person would like to contact someone that works in their division in another branch. Let's say the person is "John Doe". First, we need to know the John's `division_id` or anything that matches their role in another branch.

After we know that, we can easily find the personnel working in the same division in other branches with the query: `SELECT worker_name FROM worker WHERE worker_id = (SELECT worker_id FROM worker WHERE full_name = 'John Doe') AND worker_branch != (SELECT worker_branch FROM worker WHERE full_name = 'John Doe');`

This query should, in theory, select people working in the same division as John in other branches of the company.

# Join statements
Join statements allow you to join columns from multiple tables. The generic syntax is:
```SQL
SELECT employee_id, employee_name FROM employee e
JOIN department d on e.department_id = d.department_id
JOIN payment p on e.payment_account = p.payment_account
```
In this example, the resulting should, hopefully, join the 3 tables, allowing the user to pinpoint exactly who is getting paid, what kind of job they were doing, and how to pay them.
# Normal Forms
Normal forms are states of a database that, when fulfilled, would reduce redundancy and simplify dependencies.
## 1st Normal Forms
Every field (column) must contain only one value.

## 2nd Normal Forms
"any non- UID attribute be dependent on (be a property of, or a characteristic of) the entire UID"

When a table has a composite primary key and one of its attributes only depend on one of the primary keys (partial dependency), it does NOT fulfill 2NF. To fix this, split the primary keys to their own respective tables.

Observe the following table:
```
PRODUCT SUPPLIER {
# Supplier Number
# Product Number
* Purchase price
* Supplier Name
}
```

Purchase price depends only on product number, while supplier name only depends on product number. Since each of the non-UID fields only partially depends on the UID fields (purchase price with product number; supplier name with supplier number), we can split the table into:

```
SUPPLIER {
# Supplier Number
* Supplier Name
}

PRODUCT {
# Product Number
* Purchase Price
}
```
## 3rd Normal Forms
"no non-UID attribute can be dependent on another non-UID attribute"

If a table contains fields that depends on other fields other than the UID, it does NOT fulfill 3rd NF. 


Observe the following table:
```
EMPLOYEE {
# Employee ID
* Employee Name
* Department ID
* Department Name
}
```

Notice that both `Department ID` and `Department Name` does not depend on the UID `Employee ID`. Instead, `Department Name` depends on `Department ID` that stands alone, creating a sort of segregation where one side handles employees and the other, departments. It is better if we split the table in 2:
```
EMPLOYEE {
# Employee ID
* Employee Name
}

DEPARTMENT {
# Department ID
* Department Name
}
```