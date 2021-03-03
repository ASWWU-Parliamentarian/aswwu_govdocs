# General Information

This repository is a collection of the governing documents of the Associated Students of Walla Walla University. It is designed and hosted in such a way that encourages consistent and trackable amendments to the documents.

## LaTeX

The documents in this repository are built on a document preparation software and markup language called [LaTeX](https://en.wikipedia.org/wiki/LaTeX), which has the following benefits:

- **Separation of presentation from content**: LaTeX attempts to follow the design philosophy of separating presentation from content, so that authors can focus on the content of what they are writing without attending simultaneously to its visual appearance. In preparing a LaTeX document, the author specifies the logical structure using simple, familiar concepts such as chapter, section, table, figure, etc., and lets the LaTeX system handle the formatting and layout of these structures. As a result, it encourages the separation of the layout from the content — while still allowing manual typesetting adjustments whenever needed. This concept is similar to the mechanism by which many word processors allow styles to be defined globally for an entire document, or the use of Cascading Style Sheets in styling HTML documents.
- **Custom and consistent presentation:** LaTeX is a markup language that handles typesetting and rendering. It can be configured with custom macros that defines new environments and commands. This allows for design flexibility to obtain a professional and well-organized layout of the governing documents. Additionally, the style and layout of documents can be easily replicated to other documents for consistently of appearance and navigation.

### Useful LaTeX Commands
| Syntax    | Description   | Usage Example   |
| --------- | ------------- | --------- |
| \\$        | To type a dollar sign, you must have a backslash before the dollar sign symbol | The Atlas must retain \\$3000 of income in... |
| \\&        | To type an ampersand symbol (&), you must have a backslash before it | Inventory \\& Resource Management |
| \nth{#}    | To type have a nicely typeset 1st or 2nd, with the postfix as a superscript, use this command | The \nth{3} and \nth{4} time someone goes... |
| \textit{X} | Italics can be typeset by placing the desired italicized words in place of "X" | Refer to \textit{Robert's Rules of Order} for the process to...|


# Structure

The repository is split up into the following sections.

- **aswwu_govdocs**
    - **.github/workflows**
        - ***buildBylaws.yml*** - Workflow file to run the GitHub action that builds and compiles the LaTeX code for the Bylaws.
        - ***buildConstitution.yml*** - Workflow file to run the GitHub action that builds and compiles the LaTeX code for the Constitution.
        - ***buildSPR.yml*** - Workflow file to run the GitHub action that builds and compiles the LaTeX code for the Senate Procedural Rules.
    - **Formatting *-*** Folder containing preamble files and other formatting files
        - ***Bylaws-Preamble.tex*** - The LaTeX preamble for the Bylaws, which contains essential formatting setup, such as fonts, included packages, and defined macros.
        - ***Constitution-Preamble.tex** -* The LaTeX preamble for the Constitution, which contains essential formatting setup, such as fonts, included packages, and defined macros.
        - ***Senate_Procedural_Rules-Preamble.tex*** - The LaTeX preamble for the Senate Procedural Rules, which contains essential formatting setup, such as fonts, included packages, and defined macros.
        - ***Logo_ASWWU-Black.eps*** - The vector file of the ASWWU Logo, which is included in all governing documents.
    - ***ASWWU_Bylaws.pdf*** - The presentable and typeset version of the Bylaws
    - ***ASWWU_Bylaws.tex*** - The raw content of the Bylaws, where amendments will be made.
    - ***ASWWU_Constitution.pdf*** - The presentable and typeset version of the Constitution
    - ***ASWWU_Constitution.tex*** - The raw content of the Constitution, where amendments will be made.
    - ***ASWWU_Senate_Procedural_Rules.pdf*** - The presentable and typeset version of the Senate Procedural Rules.
    - ***ASWWU_Senate_Procedural_Rules.tex*** - The raw content of the Senate Procedural Rules, where amendments will be made.

# Training

- "$" sign
- Using square brackets for titles []
- "&" sign
- \nth{}
- Italics
- Em-dash: Three dashes "- - -"
- Bold
- Headings
- Update process
- Editing
