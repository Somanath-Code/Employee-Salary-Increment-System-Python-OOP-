class Employee:
    def __init__(self, salary, increment_percent):
        self._salary = salary
        self._increment_percent = increment_percent

    @property
    def salary(self):
        return self._salary

    @salary.setter
    def salary(self, value):
        # When salary changes, we can adjust increment dynamically
        self._salary = value
        # Example rule: higher salary → lower increment percentage
        if self._salary > 50000:
            self._increment_percent = 5
        elif self._salary > 30000:
            self._increment_percent = 8
        else:
            self._increment_percent = 10
        

    @property
    def increment(self):
        return self._increment_percent
    

    @increment.setter
    def increment(self, value):
        # Allow manual override of increment percentage
        self._increment_percent = value
        

    @property
    def salaryAfterIncrement(self):
        return self._salary + (self._salary * self._increment_percent / 100)
    
    

    
    


# Example usage:
emp = Employee(20000, 10)
print("Initial Salary:", emp.salary)
print("Increment %:", emp.increment)
print("Salary After Increment:", emp.salaryAfterIncrement)

# Update salary → increment adjusts automatically
emp.salary = 40000
print("\nUpdated Salary:", emp.salary)
print("Adjusted Increment %:", emp.increment)
print("Salary After Increment:", emp.salaryAfterIncrement)



