# Product Requirements Document (PRD): Student Companion

## 1. Overview
Student Companion is a simple web page that gives college students two tools in one place: an attendance calculator and a notice hub.

## 2. Problem statement
- **Attendance surprises.** Attendance is counted per class, not per day. In one real case, five days off in the first semester dropped attendance from 100% to 90%, and the student did not see it coming.
- **Lost notices.** Important academic material (such as lesson notes) gets buried under event announcements, so students lose track of it.

## 3. Target users
Students of Dr. Virendra Swarup Institute of Computer Studies, Kanpur. The first users are first-semester BCA students.

## 4. Goals
- Let a student know where their attendance stands before it becomes a problem.
- Keep academic notices separate from events so nothing important is lost.
- Be simple, free, and usable on a phone with no installation.

## 5. Features (version 1)

| # | Feature | What it does |
|---|---------|--------------|
| 1 | Attendance calculator | Takes classes held and attended; shows percentage, classes that can still be missed, or classes that must be attended to reach 75% |
| 2 | Days-off simulator | Takes planned days off and classes per day (default 4); shows the resulting percentage |
| 3 | Notice hub | Lists notices by category (Academics, Exams, Events, Urgent); filter by category; click a notice to see its details |

## 6. User flow
1. The student opens the link on their phone.
2. They type classes held and attended, then press Calculate.
3. They optionally enter days off to see the effect.
4. They scroll to the notice hub and filter by category to find what they need.

## 7. Assumptions
- The minimum attendance requirement is 75%.
- The college holds 4 classes per day.
- Attendance is counted over all subjects together.

## 8. Out of scope (version 1)
- Login or user accounts
- Reminders and push notifications
- Subject-by-subject attendance
- A form for adding notices (notices are sample data in the code)

## 9. Success measures
- The calculator gives correct results for valid inputs and a clear message for invalid ones.
- The page is readable and usable on a phone screen.
- A student can find a notice in the right category in a few clicks.

## 10. Future scope
Deadline reminders, per-subject attendance, timetable and exam dates, a notice form for class representatives, and optional login.
