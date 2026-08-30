# PTEC NoteBOT

**PTEC NoteBOT** is an unofficial, student-focused study portal designed for students of **Pabna Textile Engineering College (PTEC)**.

It provides a single, responsive web interface for accessing study materials, semester-wise subjects, departmental resources, lab reports, question banks, notices, routines, results, a textile-focused offline chatbot, academic utilities, and fun learning tools.

> **Note:** This is an unofficial student project and is not an official website of Pabna Textile Engineering College or Bangladesh University of Textiles.

---

## ✨ Features

### 📚 Academic Resources

* **8 semesters** from Level 1 Term I through Level 4 Term II
* Semester-wise subject organization
* Department-wise subject navigation
* Supports:

  * Yarn Engineering
  * Fabric Engineering
  * Wet Process Engineering
  * Apparel Engineering
  * Yarn + Fabric
  * Wet + Apparel
* Subject search functionality
* Individual subject resource pages
* Google Drive links for available study materials
* Lab Reports section
* Question Bank (Q-Bank) section
* Syllabus section
* Notes submission interface

The academic structure is stored directly inside the HTML application's JavaScript data section.

### 🔎 Quick Search

The built-in search system can search across:

* Semester/term names
* Subjects
* Departments
* People listed in the phone book

Search results are displayed dynamically without reloading the page.

### 🤖 Tex-GPT

PTEC NoteBOT includes a small **offline textile knowledge assistant**.

It provides predefined answers for common textile topics such as:

* Cotton
* Yarn count / Ne
* Tex
* Warp
* Weft
* Weaving
* Knitting
* Mercerization
* Carding

It works locally in the browser using a predefined knowledge base; no external AI API is required.

### 🧮 Textile Tools

The portal includes a **Count Koto** utility with:

* Stitch/row counter
* Ne ↔ Tex converter
* Textile count calculation

The Ne/Tex converter uses:

`Tex ≈ 590.5 ÷ Ne`

and automatically converts in both directions.

### 🏛️ Library & Free Courses

The portal contains sections for:

* E-book resources
* Past papers
* Reading-room information
* Free learning resources
* Spinning basics
* Weaving basics
* Dyeing & finishing introduction

These areas are currently structured as information/sample sections and can be expanded through the application's data section.

### 📢 Updates

Dedicated sections are provided for:

* Notices
* Exam routines
* Results

These are maintained as JavaScript data arrays inside the application.

### ☎️ Phone Book

The portal includes a searchable phone book containing categorized contacts such as:

* Teachers
* Staff
* Support personnel

Selecting a contact can open the phone dialer on supported devices.

### 📌 Personal Pins

Users can pin frequently used subjects or resources.

Pinned items are stored using **localStorage**, so the selections remain available in the same browser.

### 🌗 Dark / Light Mode

The interface supports:

* Dark mode
* Light mode
* Persistent theme selection

The selected theme is saved in `localStorage`.

### 🎮 Games & Fun

The portal includes several small browser-based games:

* Tic-Tac-Toe
* Rock Paper Scissors
* Memory Game
* Textile-themed jokes

Tic-Tac-Toe includes a simple CPU opponent and score tracking.

---

## 🎨 Design

PTEC NoteBOT uses a modern glassmorphism-inspired interface featuring:

* Responsive layouts
* Glass-style cards
* Gradient buttons
* Animated backgrounds
* Textile machinery doodles
* Smooth transitions
* Animated page elements
* Mobile bottom navigation
* Dark and light themes
* Reduced-motion accessibility support

The background includes textile-themed SVG illustrations such as a loom, ring spinning machine, circular knitting, stitching, yarn cone, mechanism/gear, and fiber/yarn graphics.

---

## 🛠️ Technology

PTEC NoteBOT is intentionally lightweight and does not require a backend.

### Frontend

* HTML5
* CSS3
* Vanilla JavaScript
* SVG
* CSS animations
* Responsive CSS / media queries

### Browser APIs

The project uses browser-native features including:

* `localStorage`
* `navigator.share`
* `navigator.clipboard`
* `IntersectionObserver`
* Browser `tel:` links

The application maintains its own client-side navigation system instead of relying on separate HTML pages.

---

## 📁 Project Structure

The current project can be used with a very simple structure:

```text
PTEC-NoteBOT/
│
├── index.html
├── logo.png
└── README.md
```

`index.html` contains the application's:

* HTML structure
* CSS
* JavaScript
* Academic data
* Navigation
* Tools
* Games
* Textile knowledge base

The `logo.png` file is used as the application logo and favicon.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/PTEC-NoteBOT.git
```

### 2. Open the project

Open the project folder and launch:

```text
index.html
```

You can simply open it in a modern web browser.

### 3. Run locally

No Node.js, database, backend server, or package installation is required for the current version.

For a better development environment, you can also use **VS Code + Live Server**.

---

## 🌐 Deployment

Because the application is a client-side HTML/CSS/JavaScript project, it can be hosted using services such as:

* GitHub Pages
* Netlify
* Vercel
* Cloudflare Pages
* Any standard static web hosting

For GitHub Pages:

1. Upload the project to a GitHub repository.
2. Make sure `index.html` is in the repository root.
3. Go to **Settings → Pages**.
4. Select the required branch.
5. Save the configuration.
6. GitHub Pages will generate the website URL.

---

## 📝 Updating Content

Most of the site's content is stored inside the JavaScript **DATA SECTION**.

Important variables include:

```javascript
TERMS
NOTES
REPORTS
QBANK
FILES
NOTICES
ROUTINES
RESULTS
PHONES
JOKES
TEXKB
INFO
SUBMIT_FORM_URL
```

For example, study files can be added through the `FILES` object:

```javascript
var FILES = {
    '2-2|AE|MMTF': [
        {
            t: 'MMTF Notes',
            u: 'YOUR_GOOGLE_DRIVE_LINK'
        }
    ]
};
```

The current implementation already demonstrates Google Drive resources being opened from subject pages.

---

## 📤 Adding a Note Submission Form

The application contains a `SUBMIT_FORM_URL` variable:

```javascript
var SUBMIT_FORM_URL = '';
```

Replace the empty value with your submission form URL:

```javascript
var SUBMIT_FORM_URL = 'https://forms.google.com/your-form';
```

When configured, the **Submit Notes** section provides an option to open the submission form.

---

## ⚙️ Customization

You can customize the project by editing:

### Colors

CSS variables are defined near the top of the stylesheet:

```css
--p1
--p2
--a1
--a2
--success
--warn
--err
```

### Typography

The project currently uses:

* Inter
* Hind Siliguri
* JetBrains Mono

### Academic Data

Update the JavaScript data objects to add or remove:

* Subjects
* Notes
* Lab reports
* Question banks
* Notices
* Routines
* Results
* Contacts
* Textile knowledge

---

## 📱 Responsive Design

The interface is designed to work across:

* Desktop
* Laptop
* Tablet
* Mobile phones

On smaller screens, a bottom navigation bar provides quick access to:

```text
Home
Notes
Search
Tools
More
```

The mobile navigation is enabled through responsive CSS.

---

## 🔐 Privacy & Data

The current application is primarily client-side.

There is no application backend in the provided code.

User-specific settings such as:

* Theme preference
* Pinned resources

are stored locally in the browser using `localStorage`.

The website does not require an account or login for its core functionality.

---

## ⚠️ Important Notes

* PTEC NoteBOT is an **unofficial student study portal**.
* Some resources are samples or placeholders and may need actual links/content added.
* The availability and correctness of notices, routines, results, phone numbers, and academic resources depend on the data maintained in the source code.
* The Tex-GPT feature is a predefined offline knowledge system, not a full generative AI service.
* Some sections such as Library, Free Courses, and Notes Submission are designed to be expanded through the project's data configuration.

---

## 🤝 Contributing

Contributions are welcome.

You can improve the project by:

* Adding verified study materials
* Adding missing subjects
* Adding better question banks
* Improving the textile knowledge base
* Adding useful academic calculators
* Improving accessibility
* Fixing bugs
* Improving mobile responsiveness
* Adding new student tools

Before adding academic information, make sure the content is accurate and relevant to the appropriate course or department.

---

## 📜 License

This project does not currently specify a formal open-source license.

If you plan to allow public modification and redistribution, consider adding a license such as **MIT License**.

---

## ❤️ Acknowledgement

Made with ❤️ by PTEC students.

**PTEC NoteBOT**
Pabna Textile Engineering College
Unofficial Student Project · Affiliated with BUTEX

---

## ⭐ Project Goal

The goal of PTEC NoteBOT is to make academic resources easier for PTEC textile engineering students to discover, organize, and use from a single lightweight web application.

> **Study smarter. Find faster. Prepare better. 🎯**
