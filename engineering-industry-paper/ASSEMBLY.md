# Assembling the document

When the deliverable is a DOCX, it is built from `manuscript.md`. The manuscript is authoritative and assembly gives it a format: assembly does not reinterpret the text, and adds no figure, table, equation, result, or sentence that has no source in the manuscript. Where a current DOCX already exists for this manuscript, it is reused.

## Equations

LaTeX in the manuscript becomes real mathematics in the document — native Word equations or an equivalent formal equation object. Raw LaTeX does not appear in the finished paper, and the DOCX holds no version of an equation the manuscript does not.

## Tables

Content comes from the manuscript or from a structured source recorded in the ledger, with derived values traceable to that source. Formatting — borders, alignment, widths, caption placement — is assembly's business.

## Figures

Assembly places finished assets at the size the document uses. Composing a complex technical figure out of document shapes at assembly time is the wrong end of the job: produce the asset first from a reproducible source, then place it.

## References

Format to the submission requirement. Every reference carries a role in the paper — engineering background, standing practice, a standard or specification, a technical fact, the source of a method — and is cited where it bears. A minimum reference count is met with sources that are genuinely relevant and actually used.

Where real sources cannot reach the required count, the shortfall goes to the author, named, rather than filled with references the paper does not use.

## Parity

Before delivery, extract the DOCX text and read it against the manuscript, then compare the rendered pages. Check that headings, equations, tables, numbers, identifiers, quotations, figure captions, and the reference list agree in substance. Any divergence is an assembly defect, and the manuscript decides which version is right.

## The built document

Substance agreed is not the document working. The build passes two gates: inspect the document structure mechanically, then inspect the pages as rendered. A clean conversion log or a DOCX that opens is not a pass.

- Scan extracted text and document structure for surviving LaTeX delimiters or commands, Markdown markers, missing or duplicated content, and equations that are not mathematics objects.
- Every table has every row and column inside the text block. When a table must cross a page, its header repeats and rows remain readable; long identifiers wrap without becoming ambiguous.
- Every figure is present, legible at the size printed, and inside the text block rather than overflowing or silently cropping. Claims about an asset's format or construction match the actual inserted asset.
- Headings, captions, and the reference list are styled as such rather than as body text. Pagination strands no heading from its content and leaves no figure where its text cannot reach it.
- Read the rendered pages at delivery size. Equations, punctuation, quotations, tables, and figures must look correct to the reader, not merely exist in the package.

A defect found here is fixed at its source — the manuscript, the asset, or the assembly step — and the document is rebuilt and both gates rerun. Delivery waits for a clean structural scan and rendered read.
