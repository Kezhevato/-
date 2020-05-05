# -@startuml
class Institute { 
- name: String
- list: Lecturers
+ getName(): String
+ getStudent(): List
+ addStudent(student: Student)
+ getRequest(): String 
+ getLecturers(): List 
+ addLecturer(lecturer: Lecturer) 
} 

class Course{ 
- Student: List 
- name: String 
+ Course(name: String)
+ getName(): String 
+ addStudent(student: Student) 
+ removeStudent(student: Student)
+ getStudent(): List
+ getNumberOfStudent(): int 
} 

class Lecturer { 
- name: String 
- emailAdcress: String 
- specialization: String 
+ Lecturer(name: String, emailAddress: String, specialization: String)
+ getSpecialization(): String
+ getName(): String
+ getEmailAddress() 
} 

class Student {
- id: int
- name: String
- courses: List<Course>
+ (name: String) Student
+ getId(): int
+ getName(): String
+ addCourse (course: Course)
+ getCorses(): List<Course>
}

Student --> Course
Institute --> Course
Lecturer --> Institute
@enduml
