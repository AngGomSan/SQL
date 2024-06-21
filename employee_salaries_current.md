## Current Employee Salaries

**Goal:** Pull current salary data to show the latest increases in employee salaries. Output includes their ID, first and last names, department ID, and current salary, ordered by employee ID in ascending order.

**Table:** ms_employee_salary

**ms_employee_salary**

- id: int
- first_name: varchar
- last_name: varchar
- salary: int
- department_id: int

**Query:**

```
SELECT id, first_name, last_name, department_id, MAX(salary) AS salary
FROM ms_employee_salary
GROUP BY id, first_name, last_name, department_id
ORDER BY id;
```

**Output (first 10 rows):**

```
id	first_name	last_name	department_id	  salary
1	Todd	        Wilson	        1006	          110000
2	Justin	        Simon	        1005	          130000
3	Kelly        	Rosario	        1002	          42689
4	Patricia	Powell    	1004	          170000
5	Sherry	        Golden    	1002	          44101
6	Natasha	        Swanson	        1005	          90000
7	Diane	        Gordon	        1002	          74591
8	Mercedes      	Rodriguez	1005	          61048
9	Christy        	Mitchell	1001	          150000
10	Sean	        Crawford	1006	          190000
```

<sub>*From StrataScratch coding questions.*</sub>
