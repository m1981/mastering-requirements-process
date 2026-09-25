# Word-to-Markdown Conversion Contract

## Source and scope

The source of truth is ` Mastering the Requirements Process- Getting Requirements Right, 3rd Edition.docx`. The accompanying `full-book 5.txt` is a convenience reference for locating and checking text; it does not override the Word document's structure, formatting, or image placement.

The complete conversion will preserve the book's wording and reading order as closely as practical. The Markdown version will use minimal styling and will not paraphrase or omit book content. Source files remain in the project root.

## Output layout

```text
mastering-requirements-process/
├── README.md
├── contents.md
├── front-matter/
│   ├── preface.md
│   ├── foreword.md
│   └── acknowledgments.md
├── chapters/
│   ├── 01-some-fundamental-truths.md
│   ├── 02-the-requirements-process.md
│   └── ... (through chapter 17)
├── appendices/
│   ├── appendix-a-volere-requirements-specification-template.md
│   ├── appendix-b-stakeholder-management-templates.md
│   ├── appendix-c-function-point-counting.md
│   └── appendix-d-volere-requirements-knowledge-model.md
├── back-matter/
│   ├── glossary.md
│   ├── bibliography.md
│   └── index.md
└── img/
    └── ... (extracted image assets)
```

## Naming and navigation

- Use lowercase kebab case for names. Chapter files start with a two-digit chapter number so they sort in book order.
- Keep each chapter, front-matter item, appendix, and back-matter section in its own Markdown file.
- `contents.md` is the separate table of contents and links to the corresponding Markdown files.
- `README.md` briefly explains the folder layout and how to navigate the book.
- Preserve meaningful original headings and their hierarchy. Use plain Markdown headings, paragraphs, lists, block quotes, and tables as appropriate, with minimal additional styling.

## Paragraph references

- Give each content paragraph a visible reference prefix so passages are easy to locate and cite. Use `[section-id-P001]`, with a three-digit counter that restarts at each heading. For example, paragraphs under section `1.12.1` are `[1.12.1-P001]`, `[1.12.1-P002]`, and so on.
- Paragraphs before the first numbered section use the chapter identifier, such as `[1-P001]`.
- Apply paragraph references to prose, quotations, list items, image blocks, and captions. Keep the paragraph text and reading order intact.

## Images

- Extract images from the Word file into `img/` as separate files. Use stable numbered names such as `image001.jpeg` where an original filename is not meaningful.
- Link each image from its position in the relevant chapter or other content file using a relative path, for example `../img/image001.jpeg` from a chapter file.
- Preserve the original caption alongside the image when present. Do not replace image content with a text description.

## Verification

For each converted file, compare the text, sequence, section boundaries, and image placement against the Word source. Use the companion text file as an additional check for extraction omissions or discrepancies. Record any source ambiguity or conversion limitation rather than silently changing the book.
