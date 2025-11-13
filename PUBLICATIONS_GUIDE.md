# Publications Guide

## How to Add a New Publication

Edit the file `_data/publications.yml` and add a new entry at the top (or in the appropriate year section):

```yaml
- title: "Your Paper Title"
  authors: "Last, F., & Other, S."
  year: 2025
  venue: "Journal Name"
  volume: "10(2)"  # optional
  pages: "123-145"  # optional
  doi: "10.1234/example"
  type: "journal"  # or "preprint", "conference", etc.
  pdf: "/files/paper.pdf"  # optional - path to PDF file
```

## Field Descriptions

- **title** (required): Full title of the publication
- **authors** (required): Author names, formatted as you want them to appear
- **year** (required): Publication year (used for grouping)
- **venue** (required): Journal name, conference name, or preprint server
- **volume** (optional): Volume and issue number
- **pages** (optional): Page numbers
- **doi** (required for published work): DOI for the publication
- **type** (optional): Publication type (journal, preprint, conference, etc.)
- **pdf** (optional): Path to PDF file if you want to host it locally
