---
name: engineering-paper-typesetting
description: Turn a completed engineering-paper DOCX into a submission-ready DOCX. Use when finalizing Word formatting from submission rules, templates, or reference papers while preserving the completed paper's substance and wording.
---

# Engineering paper typesetting

Format an already completed paper DOCX for submission. The input DOCX is the content authority; this skill changes its presentation, not its argument.

Begin from the completed DOCX itself. Earlier paper ledgers, manuscripts, or skill outputs are neither required nor assumed. Work on a copy and leave the supplied source unchanged.

The governing principle is **element fidelity**: identify what each document element is, determine the rule that applies to that element, and format it accordingly. A page that merely resembles a reference from a distance is not enough.

## Authority

Resolve formatting decisions in this order:

1. binding submission requirements, including mandatory rules in an official template or style guide;
2. explicit user formatting preferences that do not conflict with a binding requirement;
3. non-binding conventions in an official venue template or style guide;
4. consistent element-level conventions in supplied reference papers;
5. the source DOCX's existing formatting;
6. conservative professional defaults, used only where the higher authorities are silent.

A higher authority overrides a lower one. Record material conflicts and the chosen rule. When the user explicitly requests an override of a binding submission requirement, surface the conflict and its submission consequence rather than treating the two instructions as equal or presenting the result as compliant. Treat reference papers and templates as format evidence only: their wording, claims, names, numbers, citations, bibliography entries, headers, and other content never enter the paper.

When an unresolved ambiguity could affect acceptance or materially change the document, ask the user. Otherwise choose the narrowest consistent interpretation and record it.

## Outputs

Create a `typesetting/` directory containing:

- `format-spec.md` — the applicable rule for each document element, its authority, and any conflict resolution;
- `inspection.md` — structural and page-by-page checks, defects found, fixes made, and remaining limits;
- the submission-ready DOCX, with a distinct filename;
- a retained final render as PDF or page images.

The DOCX is the primary user-facing deliverable. Keep `format-spec.md`, `inspection.md`, and the retained render as working and verification artifacts; deliver them to the user only when requested. Keep temporary conversions and diagnostic files outside the deliverable set when practical.

## Process

### 1. Inventory the package

Locate and open the completed DOCX, every explicit requirement, and every supplied template or reference paper. Identify which artifact is the source paper, which artifacts carry binding rules, and which only demonstrate format.

Inspect the DOCX as both a Word package and rendered pages. Inventory at least:

- sections, page setup, margins, columns, headers, footers, and page numbering;
- paragraphs, named styles, direct formatting, tabs, indents, spacing, pagination controls, and lists;
- title and author blocks, abstract, keywords, headings, body text, quotations, acknowledgements, and appendices;
- figures, tables, equations, captions, footnotes or endnotes, citations, hyperlinks, cross-references, and bibliography;
- fields, bookmarks, comments, tracked changes, hidden text, embedded objects, and section breaks;
- fonts actually used, including East Asian and complex-script font settings.

Use tools that expose underlying DOCX structure where necessary; visual inspection alone cannot establish style, field, or object correctness.

**Done when** every supplied artifact has a role, the source DOCX's element inventory is complete, and any unreadable or missing binding input is surfaced.

### 2. Derive the format specification

Translate requirements and reference evidence into explicit element-level rules in `format-spec.md`. Include applicable values or conventions for:

- paper size, orientation, margins, columns, section starts, headers, footers, and pagination;
- title, subtitle, authors, affiliations, abstract, keywords, heading levels, body, lists, quotations, acknowledgements, appendices, and references;
- Latin, East Asian, mathematical, and symbol fonts; font size, weight, color, and emphasis;
- paragraph alignment, indentation, line spacing, space before and after, widow/orphan control, keep-with-next, and page breaks;
- figure and table placement, sizing, wrapping, borders, cell padding, header repetition, caption placement, numbering, and source notes;
- equation objects, alignment, numbering, punctuation, and surrounding spacing;
- citation and bibliography presentation;
- permitted file properties, metadata, comments, tracked changes, and other submission hygiene.

For reference material, inspect repeated examples of each element rather than copying one local accident. Distinguish stable conventions from content-driven variation. If references disagree, prefer the official or most consistently evidenced convention while honoring every explicit requirement.

**Done when** every element present in the source DOCX has either an applicable rule or an explicit decision to preserve its current formatting, and every rule names its authority.

### 3. Apply the specification

Format a copy of the completed DOCX. Prefer named styles and document-level settings for repeated elements; use direct formatting only for genuine exceptions. Normalize elements by semantic role so the same kind of element follows the same rule throughout.

Preserve the paper's argument, evidence, wording, data, citations, equations, figures, tables, and ordering. Content edits are limited to mechanical necessities of formatting, such as updating generated numbering or fields, removing formatting-only placeholder text, or inserting a required running element from content already present. Record every textual difference, however small, in `inspection.md` with its mechanical reason.

Preserve functional structure while formatting it: equations remain equation objects, citations and cross-references remain functional where present, hyperlinks retain their targets, tables remain tables, and images retain adequate resolution. Rebuild an element only when required to make it valid or stable, then verify its content against the source.

Use section breaks, page breaks, keep controls, widths, and spacing deliberately. Repeated blank paragraphs, spaces, or manual line breaks are not layout mechanisms unless the governing format explicitly requires them.

**Done when** the working DOCX implements every rule in `format-spec.md`, all exceptions are recorded, and no substantive content change has been introduced.

### 4. Verify structure and parity

Compare the finished DOCX directly with the source DOCX. Extract and compare text in reading order, then inspect document structure and relationships. Account for every difference, including fields whose displayed values changed.

Check at least:

- no missing, duplicated, reordered, or imported reference content;
- identical substantive wording, numbers, equations, citations, notes, captions, tables, and bibliography entries;
- valid styles, numbering, fields, links, bookmarks, media, and embedded objects;
- correct section properties, margins, headers, footers, pagination, and page-number restarts;
- no unresolved comments, tracked changes, hidden submission notes, broken references, or unintended metadata;
- fonts and symbols survive on the target rendering path, with substitutions recorded if unavoidable.

A successful save, conversion, or package validation is evidence only for that operation. It does not complete verification.

**Done when** every source-to-final difference is either pure formatting or a recorded mechanical change, and structural checks report no unexplained defect.

### 5. Inspect the final render

Render the exact final DOCX through the best available submission-relevant Word-compatible engine. Inspect every page at delivery size, including the first and last page and every page containing a table, figure, equation, footnote, reference transition, or section boundary.

Check element fidelity and page behavior:

- text is legible and uses the specified fonts, sizes, spacing, indents, and alignment;
- headings remain with their following content and pagination has no avoidable stranded lines;
- tables and figures stay inside the text area, remain legible, and break only in permitted ways;
- captions remain attached to their objects and numbering is correct;
- equations, symbols, superscripts, subscripts, punctuation, and citations render intact;
- headers, footers, columns, section changes, and page numbers appear where required;
- references have consistent hanging indents, spacing, and wrapping;
- there are no blank-page, overlap, clipping, substitution, overflow, or field-display defects.

Fix each defect at its governing source — style, section property, object setting, or local exception — then regenerate the DOCX and rerun both structural and rendered checks. The retained render must be generated from the final delivered DOCX after the last fix.

**Done when** `inspection.md` accounts for every page, every discovered defect is fixed or disclosed as a remaining limit, the final structural parity check passes, and the retained render matches the delivered DOCX.

## Delivery

Deliver the final DOCX as the primary output. Provide the retained render, `format-spec.md`, and `inspection.md` when the user requests supporting artifacts. Summarize the authorities applied, material conflict resolutions, mechanical text changes, and any remaining environment-dependent risk such as unavailable fonts or rendering differences between office suites.
