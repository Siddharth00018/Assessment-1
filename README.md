 class Student:
    def __init__(self, name):
        self.name = name
        self.marks = []
    def input_marks(self):
        num = int(input("How many subjects do you have? "))
        for i in range(num):
            mark = float(input(f"Enter marks for subject {i+1}: "))
            self.marks.append(mark)
    def calculate_percentage(self):
        total = sum(self.marks)
        percentage = total / len(self.marks)
        return total, percentage
    def assign_grade(self, percentage):
        if percentage > 90:
            return "A"
        elif percentage >= 75:
            return "B"
        elif percentage >= 60:
            return "C"
        elif percentage >= 40:
            return "D"
        else:
            return "Fail"
    def display_result(self):
        print("\n----- Student Result -----")
        print("Name:", self.name)
        print("Marks:", self.marks)
        total, percentage = self.calculate_percentage()
        grade = self.assign_grade(percentage)
        print("Total Marks:", total)
        print("Percentage:", percentage)
        print("Final Grade:", grade)
 # main program
 name = input("Enter student name: ")
 student = Student(name)
 student.input_marks()
 student.display_result(
