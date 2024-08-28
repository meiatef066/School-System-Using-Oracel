# school-data-base-project-by-forms-and-reports-
## Project Overview
The School Database Project is designed to manage and organize essential school data, including information about students,
teachers, departments, grades, and subjects. The database schema ensures data integrity, consistency, and efficient retrieval, 
making it easier to handle various school operations.

### Project Structure
The database consists of the following tables:

#### Departments (departments):
Stores department details.
Primary Key: dept_id.

#### Students (students):
Stores student information, including their department, name, phone number, date of birth, and email.
Primary Key: student_id.
Foreign Key: dep_id references dept_id in departments.
Unique Constraint: email.

#### Grades (grades):
Stores grade categories.
Primary Key: grade_id.

#### Student Grades (student_grade):
Links students to their grades, with a grade value for each subject.
Composite Primary Key: student_id, grade_id.
Foreign Keys: student_id references student_id in students, grade_id references grade_id in grades.
Check Constraint: Ensures grade_value is between 50 and 100.

#### Teachers (teachers):
Stores teacher details, including their department, name, email, and phone number.
Primary Key: teacher_id.
Foreign Key: dept_id references dept_id in departments.
Unique Constraints: email, phone_number.

#### Subjects (subjects):
Stores subject information and links each subject to a teacher and department.
Primary Key: sub_id.
Foreign Keys: teacher_id references teacher_id in teachers, dep_id references dept_id in departments.
Unique Constraint: sub_name.

#### Department-Subject Mapping (dept_sub):
Maps subjects to departments, facilitating a many-to-many relationship.
Composite Primary Key: dept_id, sub_id.
Foreign Keys: dept_id references dept_id in departments, sub_id references sub_id in subjects.

## Usage
##### Department Management: 
Add, update, or remove departments.

##### Student Management:
Manage student records, including enrollment and grade tracking.

##### Teacher Management:
Maintain teacher information and assign subjects.

##### Subject Management: 
Assign subjects to departments and teachers.

##### Grade Tracking:
Record and monitor student grades with defined constraints.

### School ERD 
![Entity reltion ship digram ](https://github.com/user-attachments/assets/0812b446-5fb0-41fd-978d-708382e4a575)

### School Normalization
![Normalization](https://github.com/user-attachments/assets/0c4368e0-6e64-456f-aeb6-d4356254d91e)


