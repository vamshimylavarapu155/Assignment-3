# 700759652- ASSIGNMENT-VAMSHI-MYLAVARAPU

Link for the recording: 

Create a class Employee and then do the following • Create a data member to count the number of Employees • Create a constructor to initialize name, family, salary, department • Create a function to average salary • Create a Fulltime Employee class and it should inherit the properties of Employee class • Create the instances of Fulltime Employee class and Employee class and call their member functions.
class Employee: no_of_employees = 0

def __init__(self, name, family_name, salary, department):
    self.name = name
    self.family_name = family_name
    self.salary = salary
    self.department = department
    Employee.no_of_employees += 1

@staticmethod
def average_salary(employees):
    total_salary = sum(employee.salary for employee in employees)
    return total_salary / len(employees)
class FulltimeEmployee(Employee): def init(self, name, family_name, salary, department): super().init(name, family_name, salary, department)

def fulltime_benefits(self):
    print("A Few benefits as a full-time Employee.")
def main(): employees = []

f1 = FulltimeEmployee("Varun", "Thabeti", 80000, "Architecture")
f1.fulltime_benefits()
employees.append(f1)

f2 = FulltimeEmployee("Kaushik", "Kante", 78000, "Archeology")
f2.fulltime_benefits()
employees.append(f2)

e1 = Employee("Harshitha", "Reddy", 90000, "Astronaut")
employees.append(e1)

e2 = Employee("Sindhu", "Kasi", 110000, "Engineer")
employees.append(e2)

print("The Average Salary:", FulltimeEmployee.average_salary(employees))
if name == "main": main()

This program defines two classes: Employee and FulltimeEmployee, where FulltimeEmployee inherits from Employee. It also demonstrates how to create instances of both classes and call their member functions as specified in your requirements.

Numpy Using NumPy create random vector of size 20 having only float in the range 1-20. Then reshape the array to 4 by 5 Then replace the max in each row by 0 (axis=1) (you can NOT implement it via for loop)
import numpy as np

x = np.random.uniform(1, 20, 20) print("Original Array: ", x)

newarr = x.reshape(4, 5) print("\nReshaped Array: ", newarr)

max_values = np.amax(newarr, axis=1).reshape(-1, 1) newarr1 = np.where(newarr == max_values, 0, newarr) print("\nArray after replacing the maximum in each row by 0:", newarr1)

np.random.uniform(1, 20, 20) generates a random vector of size 20 with float values in the range 1-20. random_vector.reshape(4, 5) reshapes the vector into a 4x5 matrix. np.argmax(reshaped_array, axis=1) finds the index of the maximum value in each row along axis=1. reshaped_array[np.arange(len(reshaped_array)), np.argmax(reshaped_array, axis=1)] = 0 replaces the maximum value in each row with 0.
