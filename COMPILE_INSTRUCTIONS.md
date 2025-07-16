# Compilation Instructions for EAP Document

This document contains instructions for compiling the Maestro Early Access Program (EAP) LaTeX document to PDF.

## Project Structure

The project is organized as follows:
```
eap_document/
├── main.tex                    # Main entry point
├── input_box.png              # Interface screenshot
├── sections/
│   ├── introduction.tex       # Introduction section
│   ├── what_is_maestro.tex    # What is Maestro section
│   └── using_maestro/
│       ├── using_maestro.tex  # Using Maestro main section
│       ├── input_box.tex      # Input box subsection
│       ├── upload_files.tex   # Upload files subsection
│       ├── settings_menu.tex  # Settings menu subsection
│       └── commands/          # Command subsections
│           ├── behaviour.tex
│           ├── memory.tex
│           ├── file_operations.tex
│           ├── utilities.tex
│           ├── scm.tex
│           └── download.tex
```

## Prerequisites

You need to have a LaTeX distribution installed. On Fedora systems, install the required packages:

```bash
sudo dnf install -y texlive-scheme-basic texlive-latex texlive-xetex texlive-collection-fontsrecommended
```

## Compilation Steps

1. Navigate to the `eap_document` directory:
   ```bash
   cd eap_document
   ```

2. Compile the main LaTeX document to PDF using pdflatex:
   ```bash
   pdflatex main.tex
   ```

3. Run the command again to ensure proper hyperlinks and outlines:
   ```bash
   pdflatex main.tex
   ```

## Output

The compilation will generate several files:
- `main.pdf` - The final PDF document
- `main.log` - LaTeX compilation log
- `main.aux` - Auxiliary file for cross-references
- `main.out` - Hyperref outline file

## Notes

- The document uses a modular structure with `\input` commands to include sections
- The `input_box.png` image must be in the main directory
- The document uses standard LaTeX packages: geometry, xcolor, hyperref, and graphicx
- The PDF will be approximately 3 pages with the Maestro interface screenshot included

## Troubleshooting

If you encounter errors:
1. Ensure all required LaTeX packages are installed
2. Verify that `input_box.png` is in the main directory
3. Check that all section files exist in their proper directories
4. Review the `main.log` file for specific error messages