# RIT iSchool Capstone and Thesis Template for Typst

This is a Typst template for RIT iSchool capstone projects and thesis proposals/reports, adapted from the official LaTeX version. It follows the formatting requirements specified by RIT's School of Information.

## Why Typst over LaTeX?
LaTeX is more mature and well supported, but Typst is modern, clean, and faster to render.

I like that you can script and use JS functions in your document. It's really nice if you're writing something with a lot of data and tables. Update a source data JSON or CSV file, and it can immediately update everywhere it's referenced in the document. Use JS to sort, group, and style your data based on logic. It helps keep content more separated from structure and style.

## Features

- Support for both **project reports** and **thesis documents**
- Support for both **proposals** and **final reports**

## Files

- `rit-ischool-template.typ` - The main template file
- `example-capstone.typ` - Example usage showing how to use the template
- `stixtwofonts/` - font files
- `README.md` - This documentation file

## Quick Start

1. Copy `rit-ischool-template.typ` to your project directory (or the official app).
2. Create a new `.typ` file for your document (e.g., `my-capstone.typ`)
3. Import and use the template. It looks like this, just update the front-matter with your own info. Arguably cleaner (and much faster to render) 

```typst
#import "rit-ischool-template.typ": *

#show: rit-ischool-capstone.with(
  title: "Your Project Title",
  author: "Your Name",
  committee-chair: "Dr. Chair Name",
  chair-title: "Professor",
  reader: "Dr. Reader Name\nAssociate Professor",
  grant-month: "May",
  grant-year: "2024",
  is-project: true,     // false for thesis
  is-proposal: true,    // false for final report
)

// Optional: Add dedication and acknowledgments
#dedication-page[
  To my family...
]

#acknowledgments-page[
  I would like to thank...
]

// Abstract content
#abstract-content[
  Your abstract goes here...
]

// Main document content
= Introduction
Your content here...
```

4. Compile with: `typst compile your-document.typ`

## Citations and Bibliography

For citations, just use Typst's built in bibliography tools. Upload a `.bib` file, and the sources will appear as you cite them in the document:
```typst
// At the end of your document
#bibliography("references.bib")
```
