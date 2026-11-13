# Student Companion

A simple, free, mobile-friendly website that helps college students keep track of two things: **their attendance** and **their notices**.

Built solo for **Ideathon 2026** at Dr. Virendra Swarup Institute of Computer Studies, Kanpur.

**Live demo:** [ https://riddhikamishra146-del.github.io/Student-companion-ideathonn/] |  [https://student-companion-ideathonn.onrender.com]

## The problem

- Attendance is counted per class, not per day. Missing a few days can drop the percentage suddenly, and students usually find out only when it is already a problem.
- Academic notices (notes, exams, deadlines) get buried under event notices in group chats.

## What it does

### 1. Attendance calculator
Enter the classes held and the classes attended. It shows:
- your current attendance percentage
- how many more classes you can miss and still stay at 75% or above
- how many classes you must attend in a row if you are below 75%

### 2. "What if I take days off?" simulator
Enter the days you plan to miss (default: 4 classes per day, editable). It shows what your percentage would become before you decide.

### 3. Notice hub
- Notices sorted into Academics, Exams, Events and Urgent
- Filter by category with a dropdown
- Click a notice to open its details

## Tech stack

- HTML, CSS and JavaScript (no frameworks, no installation)
- Hosted on GitHub Pages

## How to run it

1. Download or clone this repository.
2. Open `index.html` in any browser.

## Documents

- [PRD.md](PRD.md): what the product is and why
- [TRD.md](TRD.md): how it is built

## Current limitations

- The notices in this demo are sample data written in the code.
- Attendance numbers are typed in by the student. The college's own record stays the official one.
- The calculator assumes a 75% minimum attendance rule.

## Future scope

- Deadline reminders
- Attendance tracked subject by subject
- Timetable and exam dates
- A simple form for class representatives to add notices
- Optional login to save data

## Author

RIDDHIKA MISHRA, BCA 1st semester

