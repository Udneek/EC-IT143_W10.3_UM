# EC-IT143_W10.3_UM
Finding Top 3 Highest Paid Employee

SELECT employee_id, employee_name, department_id, employee_salary
FROM employee_salary
WHERE RANK() OVER (PARTITION BY department_id ORDER BY employee_salary DESC) <= 3
