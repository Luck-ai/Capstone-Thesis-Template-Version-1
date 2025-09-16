# LaTeX Thesis Build Instructions

This thesis uses **LuaLaTeX** and **latexmk** inside a Docker container to ensure reproducible builds. Follow the instructions for your platform below.

---

## 🚀 Windows

1. Open **PowerShell** in the project folder.
2. Run the build script to start the Docker container:

   ```powershell
   ./build.ps1
   ```

   This will start (or create) a Docker container with TeX Live.
3. Inside the container, compile your thesis using `latexmk`:

   ```bash
   latexmk -lualatex -pdf thesis.tex
   ```

   Optionally, specify a different PDF output name:

   ```bash
   latexmk -lualatex -pdf -jobname=myoutput thesis.tex
   ```

---

## 🍎 macOS / Linux

1. Open a terminal in the project folder.
2. Run the build script to start the Docker container:

   ```bash
   ./build.sh
   ```
3. Inside the container, compile using `latexmk`:

   ```bash
   latexmk -lualatex -pdf thesis.tex
   ```

   Optionally, specify a different PDF output name:

   ```bash
   latexmk -lualatex -pdf -jobname=myoutput thesis.tex
   ```

## ⚡ Live Preview / Watch Mode

Use `latexmk` in preview continuous mode (`-pvc`) to automatically recompile when the `.tex` file changes:

```bash
latexmk -lualatex -pdf -pvc thesis.tex
```

* `-lualatex` → use LuaLaTeX.
* `-pvc` → preview continuously; recompiles on file changes.
* Works well with PDF viewers that auto-refresh (Skim, SumatraPDF, Okular, etc.).

## 🖥 VS Code Setup (Optional)

Install these extensions for a better LaTeX workflow:

* [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
  Provides build commands, syntax highlighting, and PDF preview.
* [LaTeX Utilities](https://marketplace.visualstudio.com/items?itemName=tecosaur.latex-utilities)
  Adds extra commands, completions, and utilities.

## 📄 Notes

* Always use `latexmk` for compilation. This ensures proper multi-pass builds for TOC, references, and bibliography.
* Run `latexmk -c` to clean auxiliary files.
* For automatic builds with file changes, use the `-pvc` option.
