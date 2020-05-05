# -@startuml
class Institute { 
- name: String
- list: Lecturers
+ getName(): String
+ getStudent(): List
+ addStudent(student: Student)
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
+ getLecturer()
+ assignLecture()
} 

class Lecturer { 
- name: String 
- emailAdcress: String 
- specialization: String 
+ Lecturer(name: String, emailAddress: String, specialization: String)
+ getSpecialization(): String
+ getName(): String
+ getEmailAddress()
+ getCourse()
+ addCorse()
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

Institute o--> Student
Institute o--> Course
Institute o--> Lecturer
Student - Course
Course - Lecturer
@enduml
