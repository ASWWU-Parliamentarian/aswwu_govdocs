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
~~~
\article[Records]
        \section[Constitution and Bylaws]
            \subsection At least two copies of the Constitution and Bylaws shall be maintained on reserve in the Peterson Memorial Library at all times.
            \subsection The ASWWU Governing Documents shall be kept up to date and available within two weeks of any changes, including any new Senate governance legislation. Responsibility of updating the Governing Documents shall fall upon the Parliamentarian, assisted as needed by the Senate Secretary.
        \section[Proceedings]
            \subsection A complete copy of the proceedings of the ASWWU and the Senate shall be made available in the ASWWU offices. Proceedings of the ASWWU will be an accumulation of all minutes except for those of Cabinet.
        \section[Minutes]
            \subsection[Definition:] The minutes are the official transcript of a meeting as described in the current edition of \textit{Robert's Rules of Order} for parliamentary procedure.
            \subsection[Scope:] Minutes shall be taken for Senate and Executive Committee.
            \subsection[Duties:]
                \paragraph[Senate Secretary]
                    \subparagraph The Senate Secretary shall be responsible for recording minutes for Senate and Executive Committee.
                    \subparagraph Should the Senate Secretary be unable to attend such a meeting, a temporary secretary shall be appointed prior to the meeting by the Executive Vice President. Should the Senate Secretary not attend a meeting without making prior arrangements per above, the meeting shall be cancelled and considered to have no standing until such time as a secretary is present.
            \subsection[Parliamentarian:] The Chief Justice shall be charged with overseeing compliance for this article. The Chief Justice shall keep files of all such minutes, forward them to the President, and shall make them publicly available upon request of any member of the ASWWU.
        \section[Financial Records]
            \subsection A copy of the ASWWU Financial Records shall be made available to all members of the ASWWU in the ASWWU offices.
        \section[ASWWU Digital Senate Archive]
            \subsection[Content:] The ASWWU Digital Senate Archive (ADSA) will contain all official documents of the ASWWU and shall be updated with official copies of the documents required in Title 1, Article V, Section 3.
            \subsection[Preservation and development:] The Chief Justice will be responsible for the integrity of the documents in the archive. The Chief Justice will also be responsible for coordinating with the Webmaster to ensure the update of the ADSA.
            \subsection[Availability:] The Webmaster will be responsible for ensuring the availability of the online archives as well as facilitating the ongoing development and security of the ADSA.
        \section[Presidential Annual Report]
            \subsection The ASWWU President will construct a comprehensive summary of ASWWU's actions, accomplishments, and goals during their term in office. A physical and electronic copy will be delivered to the Alumni Center, Library Archives, and Student Life. Refer to Appendix C of the Personnel Manual for a listing of entities to be included.
~~~

### Useful LaTeX Commands
| Title     | Syntax    | Description   | Usage Example   |
|---------  | --------- | ------------- | --------- |
| Comments | % | To add comments in the .tex file that won't appear in the finished product, place a '%' at the beginning of the line and then type anything following it | %This section is to describe the nature of ASWWU |
| Dollar Sign | \\$        | To type a dollar sign, you must have a backslash before the dollar sign symbol | The Atlas must retain \\$3000 of income in... |
| Ampersand Symbol | \\&        | To type an ampersand symbol (&), you must have a backslash before it | Inventory \\& Resource Management |
| Number Superscripts | \nth{#}    | To type have a nicely typeset 1st or 2nd, with the postfix as a superscript, use this command | Today was little John's \nth{4} birthday! |
| Italics   | \textit{X} | Italics can be typeset by placing the desired italicized words in place of "X" | Refer to \textit{Robert's Rules of Order} for the process to...|
| Bold | \textbf{X} | Words or phrases can be made bold through this function | This is the absoluate \textbf{BEST} ice cream in Walla Walla |
| Em-dash | --- | For a long "em-dash" type three normal dashes | That was amazing---literally, so cool! |
You can learn more LaTeX basics at [this site](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes).


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
