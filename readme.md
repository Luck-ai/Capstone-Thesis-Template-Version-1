# Thesis LaTeX Template

This is a comprehensive LaTeX thesis template designed for captsone thesis. The template uses LuaLaTeX for modern font support and is organized for easy chapter management and content updates.

## Prerequisites

Before you can build and compile this thesis template, ensure you have the following software installed:

- **[MikTeX](https://miktex.org/download)** - A comprehensive LaTeX distribution for Windows, macOS, and Linux. This provides all the necessary LaTeX packages and compilers required for building the thesis document.
- **[TexStudio](https://texstudio.org/#download)** - An integrated writing environment for creating LaTeX documents. It provides syntax highlighting, auto-completion, and integrated PDF viewing.
- **[Git](https://git-scm.com/download)** - Version control system (optional, but recommended for managing the thesis versions)

## Setup Instructions

Follow these step-by-step instructions to set up your thesis compilation environment:

1. **Open TexStudio** and open the **thesis.tex** file from the root of the repository folder
2. **Configure the LaTeX Compiler:**
   - Navigate to the **Options** menu
   - Click on **Configure TexStudio**
   - In the **Build** tab, set the default compiler to **LuaLaTeX** (this enables better font rendering and modern LaTeX features)
3. **(Optional) Enable Auto-Compilation:**
   - In the **Internal PDF Viewer** tab, enable the "Auto Recompile on Save" option
   - This will automatically compile your thesis whenever you make changes and save a file
4. **Compile and View:**
   - Click the **Build & View** button (or press F5) to compile the thesis and open the generated PDF
   - LaTeX will process all chapters and generate the final thesis.pdf file

## Demo

For a quick overview of the thesis template and its output, watch the provided demo video:
- **[Demo Video](./demo.mp4)** - A video walkthrough showing how the template works, how to compile it, and the final PDF output

## Project Structure

The thesis template is organized as follows:

- **thesis.tex** - Main thesis file (start here). Contains document setup, preamble, and includes all chapters and front matter
- **chapters/** - Contains all thesis chapter files
- **images/** - Folder for all images, figures, and graphics used throughout the thesis
- **fonts/** - Custom font files for the thesis
- **references.bib** - Bibliography/References database in BibTeX format
- **abbreviations.tex** - Common abbreviations and acronyms used in the thesis
- **env.tex** - Environment and package configuration settings
- **thesis.pdf** - Compiled output PDF document

## How to Add Content

- **Add New Chapters:** Create a new .tex file in the chapters folder and include it in thesis.tex using `\input{chapters/your_chapter.tex}`
- **Add Images:** Place images in the images folder and reference them in your chapters using LaTeX graphics commands
- **Update References:** Add citations to the references.bib file and cite them in your document using `\cite{citation_key}`
- **Modify Abbreviations:** Edit abbreviations.tex to add or update terms and their acronyms


