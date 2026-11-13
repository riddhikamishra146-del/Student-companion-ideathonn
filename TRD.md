# Technical Requirements Document (TRD): Student Companion

## 1. Overview
Student Companion is a static, single-page website. It has no backend and no database. All logic runs in the user's browser.

## 2. Tech stack

| Part | Technology |
|------|------------|
| Structure | HTML |
| Styling | CSS (responsive, mobile-friendly card layout) |
| Logic | JavaScript (plain, no frameworks) |
| Version control | Git and GitHub |
| Hosting | GitHub Pages |

## 3. Project structure
```
index.html   (page, styles and scripts)
README.md
PRD.md
TRD.md
```

## 4. How it works

### 4.1 Attendance calculator
Inputs: `held` and `attended` (numbers).

- Percentage = (attended / held) x 100
- If percentage is 75 or more: classes that can still be missed = floor((4 x attended - 3 x held) / 3)
- If percentage is below 75: classes that must be attended in a row = 3 x held - 4 x attended

These come from the condition `attended / held >= 0.75`, using whole-number arithmetic to avoid rounding errors.

Validation: if held is 0 or less, attended is negative, or attended is more than held, the page shows a message asking for valid numbers.

### 4.2 Days-off simulator
Inputs: `days` and `perDay` (default 4), plus held and attended from above.

- missed = days x perDay
- new held = held + missed (attended stays the same, because the missed classes are in the future)
- new percentage = attended / new held x 100

If the new percentage is below 75, the page warns the student.

### 4.3 Notice hub
- Notices are stored in a JavaScript array of objects with `title`, `category`, `date` and `details`.
- A dropdown selects the category. The `showNotices()` function loops over the array and builds the matching HTML.
- Each notice uses the HTML `<details>` and `<summary>` elements, so it opens and closes on click without extra code.

## 5. Non-functional requirements
- Works in any modern browser on phone and desktop.
- No installation, no login, no cost.
- Readable on small screens (viewport meta tag, flexible card width).

## 6. Deployment
- Code is stored in a public GitHub repository.
- GitHub Pages serves `index.html` from the `main` branch, so every change committed to GitHub updates the live page.

## 7. Known limitations
- Notices are hard-coded sample data, so adding one means editing the code.
- Data is not saved. Refreshing the page clears the entered numbers.
- Attendance is calculated across all subjects together.

## 8. Possible next steps
- Move the notices into a form or a small database so class representatives can add them.
- Add reminders and subject-wise attendance.
- Optionally deploy on Render as an alternative host.
