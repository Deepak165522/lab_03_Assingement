class Employee:
    def __init__(self, id_no, name, age, salary):
        self.id_no = id_no
        self.name = name
        self.age = age
        self.salary = salary

class EmployeeTable:
    def __init__(self):
        self.employees = []

    def add_employee(self, employee):
        self.employees.append(employee)

    def remove_employee(self, id_no):
        for employee in self.employees:
            if employee.id_no == id_no:
                self.employees.remove(employee)
                return True
        return False

    def find_employee_by_id(self, id_no):
        for employee in self.employees:
            if employee.id_no == id_no:
                return employee
        return None

    def display_table(self):
        print("Employee Table:")
        print("ID\tName\tAge\tSalary(PM)")
        for employee in self.employees:
            print(f"{employee.id_no}\t{employee.name}\t{employee.age}\t{employee.salary}")

# Create an employee table
employee_table = EmployeeTable()

# Add employees to the table
employee1 = Employee("161E90", "Raman", 41, 56000)
employee2 = Employee("161F91", "Himadri", 38, 67500)
employee3 = Employee("161F99", "Jaya", 51, 82100)
employee4 = Employee("171E20", "Tejas", 30, 55000)
employee5 = Employee("171G30", "Ajay" , 45, 44000)

employee_table.add_employee(employee1)
employee_table.add_employee(employee2)
employee_table.add_employee(employee3)
employee_table.add_employee(employee4)
employee_table.add_employee(employee5)
