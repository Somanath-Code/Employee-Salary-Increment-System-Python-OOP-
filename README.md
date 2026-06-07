# Employee-Salary-Increment-System-Python-OOP-
 A simple Python class demonstrating object-oriented programming concepts with properties, setters, and dynamic rules. 
 Tracks employee salary and increment percentage  Automatically adjusts increment based on salary ranges  Allows manual override of increment percentage  Calculates salary after increment

---

## Features
- Track employee salary and increment percentage
- Automatically adjust increment % when salary changes:
  - Salary > 50,000 → 5%
  - Salary > 30,000 → 8%
  - Salary ≤ 30,000 → 10%
- Allow manual override of increment percentage
- Calculate salary after increment

---

## Example Usage

```python
from employee import Employee

# Create employee with base salary and increment %
emp = Employee(20000, 10)
print("Initial Salary:", emp.salary)                # 20000
print("Increment %:", emp.increment)                # 10
print("Salary After Increment:", emp.salaryAfterIncrement)  # 22000

# Update salary → increment adjusts automatically
emp.salary = 40000
print("\nUpdated Salary:", emp.salary)              # 40000
print("Adjusted Increment %:", emp.increment)       # 8
print("Salary After Increment:", emp.salaryAfterIncrement)  # 43200

# Another employee
e = Employee(30000, 10)
print("\nBase Salary:", e.salary)                   # 30000
print("Salary After Increment:", e.salaryAfterIncrement)    # 33000
