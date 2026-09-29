# Class Management System

This is my first semester python project. It is a class attendance program where you can mark attendance for a class, add a new student and see who has low attendance, and everything is done with a menu.

I made it using only basic python, so there are no functions and no modules in it.

## What it does

- Shows a menu again and again until you choose Quit
- Mark attendance for a new class, the program asks yes or no for every student
- If you type something other than yes or no it asks again
- After marking, it works out each student's attendance percentage and shows "Low attendance" if someone is below 75%
- You can add a new student and tell how many classes they have attended till now
- Adding a student with an empty name, a name that already exists, or a wrong number of classes shows a message
- If you type something wrong in the menu it shows a message and doesnt crash

## How to run

1. Open the notebook in jupyter (or vscode)
2. Run the first cell, it has the attendance list and the total number of classes
3. Run the second cell, this starts the menu
4. Type your choice in the box and press enter
5. Choose 3 to quit

If you change something in the first cell, run it again before the second one.

## Menu

```
What do you want to do?
1) Mark attendance
2) Add a student to class
3) Quit
```

1) Mark attendance - the total number of classes goes up by 1, then for every student you type yes or no. Everyone who is marked yes gets 1 more class attended. At the end the percentage of every student is checked.

2) Add a student to class - type the name, then how many classes the student has attended till now. The number must be between 0 and the total number of classes so far.

3) Quit - ends the program

## Students and attendance

Total classes at the start: 15

| Student | Classes attended |
| --- | --- |
| Student1 | 12 |
| Student2 | 15 |
| Student3 | 14 |
| Student4 | 10 |
| Student5 | 11 |

## Example run

```
What do you want to do?
1) Mark attendance
2) Add a student to class
3) Quit
Enter your choice: 1
Attendance for class number 16
Student1 present? (yes/no): yes
Student2 present? (yes/no): yes
Student3 present? (yes/no): no
Student4 present? (yes/no): no
Student5 present? (yes/no): yes
Attendance so far
Low attendance
```

Here Student4 has attended 10 out of 16 classes (62.5%), which is below 75%, so the low attendance message is shown.

## What I used

dictionaries, while and for loops, if/elif/else, break and continue, input(), isdigit(), int(), round(), lower() and strip()

The attendance is a dictionary (student name : classes attended) and the total number of classes is kept in a separate variable, like this:

```python
Class_attendance_list={'Student1':12, 'Student2':15, 'Student3':14, 'Student4':10, 'Student5':11}
Total_classes=15
```

The percentage is worked out as classes attended divided by Total_classes times 100.

## Problems / things to add later

- The "Low attendance" message does not show the name of the student or the percentage yet, the percentage is calculated but not printed
- The attendance is lost if you restart the notebook because nothing is saved in a file
- The initial students are written in the first cell, so they can only be changed by editing it
- There is no option to see attendance without marking a new class, or to remove a student
- Names are checked exactly as typed, so "student1" and "Student1" count as different students
- Can use functions to make the code shorter once we learn them
