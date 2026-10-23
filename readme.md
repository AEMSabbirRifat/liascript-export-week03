# One-Click Course Export: LiaScript → PDF + SCORM (Week 03 lesson)

[![LiaScript Export](https://github.com/AEMSabbirRifat/liascript-export-week03/actions/workflows/main.yml/badge.svg)](https://github.com/AEMSabbirRifat/liascript-export-week03/actions/workflows/main.yml)
[![Open the course](https://img.shields.io/badge/Open_the_course-LiaScript-0A66C2)](https://liascript.github.io/course/?https://raw.githubusercontent.com/AEMSabbirRifat/liascript-export-week03/main/week03_.md)

**From one Markdown file to a printable handout and a Moodle-ready package, with no copy-pasting.**

This repository applies my LiaScript export pipeline to a second lesson. A **GitHub Actions** workflow renders the lesson and publishes:

- 📄 a **PDF handout** for students
- 📦 a **SCORM 1.2 package** for Moodle, ILIAS or OPAL

Both are attached to a versioned **GitHub Release**.

## 📘 The lesson

[`week03_.md`](week03_.md): **Research Design and Sampling Methods**, week 3 of the Quantitative Research Methods course at Otto von Guericke University Magdeburg. It covers:

- descriptive, correlational, experimental and quasi-experimental research designs
- control and manipulation, validity and reliability, data-collection methods
- probability vs. non-probability sampling, sample size and representativeness
- two interactive tasks: *Identify the research design* and a *Sampling procedures quiz*

→ [**Open it interactively**](https://liascript.github.io/course/?https://raw.githubusercontent.com/AEMSabbirRifat/liascript-export-week03/main/week03_.md)

## ⚙️ How it works

| File | Purpose |
|---|---|
| [`.github/workflows/main.yml`](.github/workflows/main.yml) | CI workflow: Node 20 → install → export → GitHub Release |
| [`scripts/generate-pdf.js`](scripts/generate-pdf.js) | Calls the official `@liascript/exporter` for PDF and SCORM |
| [`package.json`](package.json) | One place to set which lesson to export and the output name |
| [`Media/`](Media) | Diagrams used in the lesson |

**Run it:** *Actions* → *LiaScript Export* → *Run workflow* → enter a version such as `v1.1.0`.
**Run locally:** `npm install && npm run generate-pdf`

## 🔧 2026 update

The pipeline now uses the official LiaScript exporter, so the PDF shows the rendered course instead of raw Markdown, and it also builds a SCORM package. I added a shared config and a `.gitignore`, and upgraded to Node 20.

## 🧰 Skills demonstrated

`GitHub Actions` · `Automation` · `Docs-as-code` · `SCORM / LMS integration` · `Research design & sampling`

> See also: [liascript-export-week02](https://github.com/AEMSabbirRifat/liascript-export-week02) (Week 02 lesson, full pipeline write-up) · [QuRM-WiSe2024-25](https://github.com/AEMSabbirRifat/QuRM-WiSe2024-25) (all course lessons)

---

### 📬 About me

I'm **Sabbir Rifat**, an analyst and quantitative researcher who turns manual processes into reliable automated workflows.
**[a.e.m.sabbirrifat@gmail.com](mailto:a.e.m.sabbirrifat@gmail.com)** · [LinkedIn](https://www.linkedin.com/in/aemsabbirrifat) · [Portfolio](https://scaleupwithsabbir.github.io/)
