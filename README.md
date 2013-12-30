README
   
Created on Oct 14, 2013 by Mitchell Tang and Zheyuan Liu

Friendly reminder : All the scripts recognizes the database under the name "191_sample.csv" within the same directory. Please feel free to change the pathname for the database file.

Name: add_student.sh
Usage: ./add_student.sh [pennkey] [last_name] [first_name]
Description: update the database with a new row that takes in the student' pennkey, last name, and first name; the student's grades for all the missing assignments are zeros; 
script will notify if the action is successful or if any of three arguments are missing 

Name: remove_student.sh
Usage: ./add_student.sh [pennkey]
Description: with permission, removes a student that matches the pennkey along with all the existing grades
script will notify if the action is successful or if the student is not found

Name: add_an_assignment.sh
Usage: ./add_an_assignment.sh [assignment_label]
Desctiption: updates the database with a new assignment; the user will be prompted to enter the max score for the assignment; all the students' grades for this assignment will be set as 0.
script will notify if the action is successful

Name: add_student_grade.sh
Usage: ./add_student_grade.sh [pennkey] [assignment_label]
Description: the user will be prompted to enter the student's score for the assignment; updates the database with the new assignment score
script will notify if the action is successful or if the student or assignment is not found


Name: get_student_grade.sh
Usage: ./get_student_grade.sh [pennkey]
Description: outputs complete grade information for the selected student including grade total
script will notify user if student is not found

Name: get_all_student_grade.sh
Usage: ./get_all_student_grades.sh [database_path]
Descriptionoutputs grade totals for all students in the database
script will notify user if no students found
 
Name: generate_one_grade_file.sh
Usage: ./generate_one_grade_file.sh [pennkey] [assignment label]
Description: creates a grade report for a given pennkey and assignment. Files will be put in assignment directories with file name: [pennkey]_[assignmentlabel]_grade
script will notifiy user if assignment label or student was not found

Name: generate_all_student_grades.sh
Usage:./generate_all_student_grades.sh [assignment label]
Description: creates a grade reports for all students for a given assignment. Files will be put in assignment directories with file name: [pennkey]_[assignmentlabel]_grade/
script will notifiy user if assignment label was not found

Name: email_single_student.sh
Usage: ./email_single_student.sh [pennkey] [assignment label]
Desctipion: sends an email to the given student giving them a grade report for the given assignment label
script will notify user if assignment label or student was not found

Name: email_all_students.sh
Usage: ./email_all_students.sh [assignment label]
Description: sends an email to all students in the database giving them a grade report for the given assignment label
script will notify user if assignment label was not found

Name: archive.sh
Usage: ./archive.sh [term] [year]
Description: archives all assignment directories into a gzipped tar file titled year_term_backup.tar.gz