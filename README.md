# Mueller Report NLP Analysis

This repo contains the data and results of our NLP-based Mueller Report Analysis, Knowledge Graphs, entitites, relations, and so on.

Results will be published incrementaly as we identify them.

This is a collaborative effort between:

- [The NLP-Lab](https://nlp-lab.org/)
- [Semiring Inc.](https://semiring.com)
- numerous volunteers...


## Team

The team consists of:

- Damir Cavar
- Stefan Geissler
- Maanvitha Gongala
- Joshua Herring
- Mureli Kammili
- Chaitanya Patil
- S Panicker
- Umang Mehta


## Log

### 04/18/2019

In the pre-rocessing phase we prepared the two Mueller report volumes to be able to run corpus analyses on them. This is what we did after the document was published on the 18th of April.

We converted the PDF to an editable raw text format:

- The raw text has been generated in two ways:
  - We used Adobe Acrobat to OCR the text and export the raw Unicode encoded text.
  - We 
- A paragraph is one line of text preceded and followed by an empty line.
- Footnotes are tagged in the text and a footnote text is a paragraph that starts with a footnote tag <FN#>.
- Section titles are paragrpahs that start with a <SECTION> tag.
- Redacted portions of text are tagged with a <REDACTED> tag.
- We removed words and characters that were surrounded by square brackets (e.g. [T]he...).

We annotated the footnotes in the text (a lot of footnotes) using a tag in the text:

  <FN#>

where # is the number of the footnote, eg. <FN1011>. The footnote text itself is a paragraph that starts with a <FN...> tag. We left the footnotes in the text where they appeared, but we merged broken paragraphs to be continuous, if a footnote appeared within a paragraph.

The <SECTION> and <FN#> tags allow us to filter these paragraphs when running analyses over the corpus.
