<div align="center">

# 📘 Capstone Thesis LaTeX Template

**A modern LuaLaTeX thesis template — modular chapters, Biber citations, Thai-script font support, one-key build in TeXstudio.**

[![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTeX-008080?style=for-the-badge&logo=latex&logoColor=white&labelColor=0E1626)](https://www.latex-project.org/)
[![Editor](https://img.shields.io/badge/Editor-TeXstudio-22D3EE?style=for-the-badge&labelColor=0E1626)](https://texstudio.org/)
[![Bibliography](https://img.shields.io/badge/Bibliography-Biber-5A8DFF?style=for-the-badge&labelColor=0E1626)](http://biblatex-biber.sourceforge.net/)
[![Platforms](https://img.shields.io/badge/Windows%20·%20macOS%20·%20Linux-Cross%20platform-34D399?style=for-the-badge&labelColor=0E1626)](#-requirements)
[![License](https://img.shields.io/badge/License-MIT-FB7185?style=for-the-badge&labelColor=0E1626)](LICENSE)

</div>

---

## 🎯 What is it

A ready-to-use **LuaLaTeX** template for capstone / undergraduate thesis documents. Drop in your chapters, run F5 in TeXstudio, get a polished PDF. Ships with the **TH Sarabun** font set, a chapter-per-file layout, modular environment configuration, and a Biber-based bibliography.

---

## ✨ Features

- 📚 **Modular chapter-based structure** — one `.tex` per chapter under `chapters/`
- 🔤 **LuaLaTeX font support** — full Unicode + modern typography
- 🇹🇭 **TH Sarabun** font bundled (regular / bold / italic / bold-italic)
- 🖼 Organized **image & asset management** under `images/`
- 📖 Integrated **Biber** citation system
- ⚡ One-key build with **TeXstudio**
- 🧩 Separate **configuration** (`env.tex`) and **content**

---

## 📦 Requirements

| Software | Purpose | Notes |
|---|---|---|
| **[MiKTeX](https://miktex.org/download)**           | LaTeX distribution | Cross-platform — handles package install on first build |
| **[TeXstudio](https://texstudio.org/#download)**    | LaTeX editor       | Linux: `sudo apt install texstudio` |
| **[Git](https://git-scm.com/download)** *(optional)* | Version control    | Recommended for collaborative work |

---

## 🚀 Setup

### 1️⃣ Open the project

Open **TeXstudio** and load `thesis.tex` (the main document).

### 2️⃣ Configure the compiler

`Options → Configure TeXstudio → Build`

```
Default Compiler          → LuaLaTeX
Default Bibliography Tool → Biber
```

LuaLaTeX gives you better font rendering, full Unicode, and modern LaTeX features. Biber handles the bibliography.

### 3️⃣ Auto-recompile *(optional)*

`Options → Configure TeXstudio → Internal PDF Viewer → Auto Recompile on Save`

### 4️⃣ Build the thesis

Press **F5** (Build & View). Output goes to `thesis.pdf`.

---

## 🗂 Project structure

```text
Capstone-Thesis-Template-Version-1/
├── thesis.tex           # Main thesis file
├── env.tex              # Environment configuration
├── abbreviations.tex    # Acronyms
├── references.bib       # Bibliography
├── chapters/            # One .tex per chapter
├── images/              # Figures and graphics
├── fonts/               # TH Sarabun + custom fonts
└── thesis.pdf           # Compiled document
```

---

## ✍️ Adding content

### Add a chapter

Create `chapters/<name>.tex` and include it in `thesis.tex`:

```latex
\input{chapters/introduction.tex}
```

### Add an image

Drop the file in `images/` and reference it:

```latex
\includegraphics[width=\linewidth]{images/example.png}
```

### Add a reference

Add a BibTeX entry to `references.bib`:

```bibtex
@article{example2024,
  title  = {Example Paper},
  author = {Author, A},
  year   = {2024}
}
```

Cite with `\cite{example2024}`.

### Modify abbreviations

Edit `abbreviations.tex` — add or update acronyms as needed.

---

## 🧪 Debugging build errors

If TeXstudio's build silently fails, compile from the command line — the raw output makes errors much easier to diagnose:

```bash
lualatex thesis.tex
biber    thesis
lualatex thesis.tex
lualatex thesis.tex
```

Helps with **missing packages**, **font errors**, **syntax errors**, and **incorrect file paths**.

---

## 🆘 Common issues

<details>
<summary><b>MiKTeX path not set (Linux)</b></summary>

If compilation fails, MiKTeX binaries may not be on your `PATH`. Check **MiKTeX Console** for path warnings, then:

```bash
echo 'export PATH="$PATH:$HOME/bin"' >> ~/.bashrc
source ~/.bashrc
```
</details>

<details>
<summary><b>Cambria Math font not found</b></summary>

LuaLaTeX requires **Cambria Math**:

1. Download the `.ttf`.
2. Open the file and click **Install**.
</details>

<details>
<summary><b>Compilation fails due to missing packages</b></summary>

In **MiKTeX Console** → `Settings → Package Installation`, set:

```
Install missing packages on-the-fly → Always
```

Then rebuild.
</details>

<details>
<summary><b>Missing package errors</b></summary>

If you see `File 'kvoptions.sty' not found` or similar, update packages in **MiKTeX Console → Updates** and rebuild.
</details>

<details>
<summary><b>Bibliography compilation errors</b></summary>

Ensure **Biber** is installed and selected in `Options → Configure TeXstudio → Build → Default Bibliography Tool → Biber`. For manual builds:

```bash
lualatex thesis.tex
biber    thesis
lualatex thesis.tex
lualatex thesis.tex
```
</details>

---

## 💡 Tips

- Always compile with **LuaLaTeX**
- Keep chapters modular — one file each
- Store images inside `images/`
- Avoid editing `env.tex` unless you have a reason

---

<div align="center">

**Capstone Thesis Template** · [GitHub](https://github.com/Luck-ai/Capstone-Thesis-Template-Version-1) · [Issues](https://github.com/Luck-ai/Capstone-Thesis-Template-Version-1/issues)

</div>
