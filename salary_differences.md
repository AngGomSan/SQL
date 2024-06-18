## Salary Differences

**Goal:** Calculate the difference between the highest salaries found in the marketing and engineering departments and output just the absolute difference.

**Tables:** db_employee, db_dept

**db_employee**

- id: int
- first_name: varchar
- last_name: varchar
- salary: int
- department_id: int

**db_dept**

- id: int
- department: varchar

**Query:**

```
SELECT ABS((SELECT MAX(salary)
            FROM db_employee AS e
            JOIN db_dept AS d
            ON e.department_id = d.id
            WHERE department = 'engineering')
        - (SELECT MAX(salary)
            FROM db_employee AS e
            JOIN db_dept AS d
            ON e.department_id = d.id
            WHERE department = 'marketing')) AS salary_diff;
```

**Output:**

```
salary_diff
2400
```

*From StrataScratch coding questions.*
