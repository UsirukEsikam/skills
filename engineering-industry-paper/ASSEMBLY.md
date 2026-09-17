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

Before delivery, read the two side by side and check that headings, equations, tables, numbers, figure captions, and the reference list agree in substance. Any divergence is an assembly defect, and the manuscript decides which version is right.

## The built document

Substance agreed is not the document working. Open the DOCX and inspect what the reader will actually receive — a rendered read of its pages where the environment allows, and the document's own structure where that is cheaper:

- Every equation is a mathematics object, not LaTeX source, literal markup, or plain text that reads correctly and computes wrong.
- No Markdown survives as visible text — no `**`, `##`, `|` rows, or backticked spans.
- Every table reaches the page whole: header with its rows, every row and column present, inside the text block, nothing spilling past the margin.
- Every figure is present, legible at the size printed, and inside the text block rather than overflowing it or silently cropped.
- Headings, captions, and the reference list are styled as such rather than as body text, and pagination strands no heading from its content, splits no table header from its rows, and leaves no figure where its text cannot reach it.

A defect found here is fixed at its source — the manuscript, the asset, or the assembly step — and the document is rebuilt, so the manuscript stays the source of truth.
