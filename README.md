# 📚 Student Grade Calculator
### Complete Project — File-by-File Explanation

---

## 📁 Project Folder Structure

```
grade-calculator/
│
├── index.html        ← Main page (open this in browser)
├── README.md         ← This explanation file
│
├── css/
│   └── style.css     ← All visual design & styling
│
└── js/
    └── app.js        ← All logic, calculation & data
```

---

## 📄 File Explanations

---

### 1. `index.html` — The Main Page
**What it does:**
- This is the file you open in your browser
- It contains the page structure (layout skeleton)
- It links to `css/style.css` for design
- It links to `js/app.js` for logic
- Contains all input fields, buttons, result section, and records table

**Key sections inside:**
| Section | Purpose |
|---|---|
| `<head>` | Links CSS file + Google Fonts |
| Student Info fields | Name + Roll Number inputs |
| Subject fields | 5 subject mark inputs (0–100) |
| Buttons | Calculate + Reset |
| Result section | Shows Total, Percentage, Grade |
| Records Table | Shows all saved student entries |
| `<script src="js/app.js">` | Loads the JavaScript file |

---

### 2. `css/style.css` — All Visual Styling
**What it does:**
- Controls colors, fonts, spacing, layout
- Makes the dark professional UI
- Handles hover effects, animations, responsive design

**Key parts inside:**
| Part | Purpose |
|---|---|
| `:root { --variables }` | Color & size settings (edit here to change theme) |
| `body` | Centers card on screen, dark background |
| `.card` | The main white/dark box |
| `.field input` | Styled input boxes with glow on focus |
| `.btn-calc` | Blue calculate button |
| `.btn-reset` | Gray reset button |
| `.grade-circle` | Circular grade badge |
| `.grade-ap/.grade-a...` | Color per grade (teal=A+, blue=B, red=F) |
| `table` | Records table styling |
| `@keyframes` | Animations (pulse dot, slide-up result) |

---

### 3. `js/app.js` — All Logic & Features
**What it does:**
- Reads values from input fields
- Validates inputs (empty check, 0–100 range)
- Calculates total marks and percentage
- Determines grade based on percentage
- Saves all records using localStorage (browser memory)
- Renders records table with delete option

**Key functions inside:**
| Function | Purpose |
|---|---|
| `getGradeData(pct)` | Returns grade A+/A/B/C/D/F based on % |
| `validate()` | Checks all fields are filled correctly |
| `calculate()` | Main function — runs on button click |
| `resetForm()` | Clears all inputs and result |
| `renderTable()` | Draws the records table on screen |
| `deleteRecord(id)` | Removes one student row |
| `clearAllRecords()` | Wipes all saved data |
| `saveRecords()` | Saves to localStorage (survives refresh) |

---

## 🎯 Grade Logic
| Percentage | Grade | Label |
|---|---|---|
| 90% – 100% | A+ | Outstanding |
| 80% – 89% | A | Excellent |
| 70% – 79% | B | Good |
| 60% – 69% | C | Average |
| 50% – 59% | D | Below Average |
| Below 50% | F | Fail |

---

## ✅ Features
- ✅ Student Name + Roll Number
- ✅ 5 Subject marks (0–100 each)
- ✅ Auto-calculates Total, Percentage, Grade
- ✅ Color-coded grade badge
- ✅ All records shown in table
- ✅ Delete individual records
- ✅ Clear all records button
- ✅ Data saved even after page refresh (localStorage)
- ✅ Works fully offline — no internet needed
- ✅ Responsive for mobile screens

---

## 🚀 How to Run
1. Extract the ZIP file
2. Open the `grade-calculator` folder
3. Double-click `index.html`
4. It opens in your browser instantly ✅

> **No server, no installation, no internet required!**

---

## 🛠 How to Customize
| Want to change | Edit this file | Find this part |
|---|---|---|
| Colors / Theme | `css/style.css` | `:root { --variables }` |
| Fonts | `index.html` | Google Fonts link in `<head>` |
| Grade percentages | `js/app.js` | `getGradeData()` function |
| Number of subjects | `index.html` + `js/app.js` | Add input fields + update marks array |
| Max marks per subject | `js/app.js` | Change `500` to new total |
