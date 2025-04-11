## Employee_of_the_Month

This Python project determines the Employee of the Month based on the total number of hours worked by each employee. The employee with the highest recorded hours is awarded the title. In the event of a tie, where two or more employees have worked the same number of hours, they will share the award.

We will use Python function to achieve the needed goal.

```python
def employee_check(work_hours):
    #work_hours is a list of tuples
    current_max_hour = 0
    # current_max_hour retain maximum hour when running through hours worked by each staff
    hours_worked =[]
    # hours_worked helps to save hours in a list
    employee_of_month = []
    # employee_of_month helps save employees name with maximum hour in a list
    for employee,hours in work_hours:
    # This helps to run through each tuple in the list
        if current_max_hour == hours:
        #It checks if employee hour is the same as current maximum hour          
            employee_of_month.append(employee)
            #It add the name of the of the employee with same hour as the maximum hour
            hours_worked.append(hours)         
            #It add the hour worked as that of the current maximum hours worked
        elif hours > current_max_hour:
        #this checks the current employee hour is more than the current maximum hour 
            employee_of_month.clear()
            hours_worked.clear()
            current_max = hours
            employee_of_month.append(employee)
            hours_worked.append(hours)
        else:
            pass
            #In the case where the hour isn't the same or not more than maximum hour then it is irrelevant 
    return list(zip(employee_of_month,hours_worked))
    #this helps to return a list of tuple(s) 
```
