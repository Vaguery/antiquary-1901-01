# Project-specific styles

## Block styles

- `{:.publication-date}` is a block style for isolated one-line dates in the topmatter of a magazine issue
- {:.inscription} is to be a blockquote style, with no initial indents

## Inline styles

- asterisks vs. underscores: Kramdown recognizes both underscores and asterisks for marking up italicized and bold text, but locks in the editorial decision that all "italics" (indicated by single underscores or asterisks) will be rendered in HTML as `<em>...</em>`, and all "bold" (double underscores or asterisks) as `<strong>...</strong>`. In these old books, italics and bold typefaces are sometimes used not for emphasis but typographic indication, such as for book titles, foreign phrases, &c. Since the HTML5 standard suggests the use of `<i>...</i>` markup for these items, I'm thinking we'll end up using 
  - `_single underscores_` with an inline style for `<i>italic</i>{:.style}`
  - `*single asterisks*` for textual emphasis
  - something equivalent, if needed, for "bold" (though see `{:.first-word} below`)
- `{:.first-word}` The first word of some articles is sometimes set in small caps. Mark it up as `**bold**` with double asterisks so it has a graceful fallback on systems lacking small-caps typography, and follow it immediately with `{:.first-word}`: `**Like**{:.first-word} this`
- `{:.scaps}` This is a placeholder introduced by the post-processing OCR scripts, just to mark locations the OCR software has managed to perceive small caps type in the original document. It should be replaced with a more appropriate semantic style definition.
- `{:.title}` A bit of semantic sugar for italicized titles of works. As a matter of convention, I've been changing the asterisk 