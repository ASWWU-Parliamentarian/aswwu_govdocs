# General Information

This repository is a collection of the governing documents of the Associated Students of Walla Walla University. It is designed and hosted in such a way that encourages consistent and trackable amendments to the documents.

## LaTeX

The documents in this repository are built on a document preparation software and markup language called [LaTeX](https://en.wikipedia.org/wiki/LaTeX), which has the following benefits:

- **Separation of presentation from content**: LaTeX attempts to follow the design philosophy of separating presentation from content, so that authors can focus on the content of what they are writing without attending simultaneously to its visual appearance. In preparing a LaTeX document, the author specifies the logical structure using simple, familiar concepts such as chapter, section, table, figure, etc., and lets the LaTeX system handle the formatting and layout of these structures. As a result, it encourages the separation of the layout from the content — while still allowing manual typesetting adjustments whenever needed. This concept is similar to the mechanism by which many word processors allow styles to be defined globally for an entire document, or the use of Cascading Style Sheets in styling HTML documents.
- **Custom and consistent presentation:** LaTeX is a markup language that handles typesetting and rendering. It can be configured with custom macros that defines new environments and commands. This allows for design flexibility to obtain a professional and well-organized layout of the governing documents. Additionally, the style and layout of documents can be easily replicated to other documents for consistently of appearance and navigation.

### Section Hierarchy

Within this framework, there are 6 levels of section hierachies:
| Depth | Section Name | Syntax with Title (X) | Syntax without Title | Usage example |
| ------| ----------- | ------------ | ---------- | ------------ |
| 0 | Title | \title[X] | \title | \title[Habitant] This is an introduction... OR \title This is an introduction... |
| 1 | Article | \article[X] | \article | \article[Tempus] Lorem ipsum dolor sit amet |
| 2 | Section | \section[X] | \section | \article[Turpis] Lorem ipsum dolor sit amet|
| 3 | Subsection | \subsection[X] | \subsection | \subsection[Maximus] Lorem ipsum dolor sit amet |
| 4 | Paragraph | \paragraph[X] | \paragraph | \paragraph[Donec] Lorem ipsum dolor sit amet |
| 5 | Subparagraph | \subparagraph[X] | \subparagraph | \subparagraph[Mauris] Lorem ipsum dolor sit amet |

Therefore, below is a snippet of a passage from the Bylaws (not updated) to illustrate how this syntax is used:
`
    \article[External Relations]
            \section[Adventist Intercollegiate Association]
                \subsection[Purpose]
                    \paragraph The Adventist Intercollegiate Association (AIA) is a self-governing body with membership consisting of the student governments from all North American Seventh-day Adventist (SDA) colleges and universities. Its purpose is to, first, provide a forum for the discussion of shared collegiate concerns and a united voice in expressing these concerns to those in positions to bring results, and, second, to provide workshops for the exchange of ideas between colleges in order to foster activities. AIA's activities occur at an annual convention held in early spring.
                \subsection[Relations with AIA]
                    \paragraph The ASWWU is a member of AIA, and as such it is responsible for paying annual dues as specified in the AIA Bylaws.
                \subsection[Delegate Selection]
                    \paragraph The delegates to AIA's annual convention are selected by the President and are ratified by Senate.
                    \paragraph In order to properly represent the entire ASWWU student government, delegates to the AIA convention must be selected to represent each of the following ASWWU branches:
                        \subparagraph \textbf{Executive:} Outgoing and incoming Presidents
                        \subparagraph \textbf{Legislative:} Outgoing and incoming Executive Vice Presidents
                        \subparagraph \textbf{Social:} Outgoing and incoming Social Vice Presidents
                        \subparagraph \textbf{Spiritual:} Outgoing and incoming Spiritual Vice Presidents
                    \paragraph Exceptions may be approved by Senate when circumstances warrant and when requested by the President.
                    \paragraph A complete list of proposed delegates must be submitted to Senate for ratification by the next full week after ASWWU elections.
                    \paragraph The ASWWU Sponsor must attend the convention with the ASWWU delegates, but in cases where this is not possible, he/she should appoint a faculty or staff member as the trip advisor.
`

### Useful LaTeX Commands
| Title     | Syntax    | Description   | Usage Example   |
|---------  | --------- | ------------- | --------- |
| Dollar Sign | \\$        | To type a dollar sign, you must have a backslash before the dollar sign symbol | The Atlas must retain \\$3000 of income in... |
| Ampersand Symbol | \\&        | To type an ampersand symbol (&), you must have a backslash before it | Inventory \\& Resource Management |
| Number Superscripts | \nth{#}    | To type have a nicely typeset 1st or 2nd, with the postfix as a superscript, use this command | Today was little John's \nth{4} birthday! |
| Italics   | \textit{X} | Italics can be typeset by placing the desired italicized words in place of "X" | Refer to \textit{Robert's Rules of Order} for the process to...|
| Em-dash | --- | For a long "em-dash" type three normal dashes | That was amazing---literally, so cool! |


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
