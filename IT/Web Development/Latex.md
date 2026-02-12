# Getting Started
1. **Document Structure**
```tex
\documentclass[options]{class}
...
\begin{document}
. . . \name[parameter]{mandarg}...
\end{document}
```
- Special characters like `& $ % ~ { } # ^` have specific meanings and must be escaped with a backslash `\` to be printed as text.

2. **Environment**
```tex
\begin{environment}
...
\end{environment}
```

3. **Declarations:** These are commands that change parameters (like margins or font size) without printing text directly. Their effect lasts until another declaration changes it or the current environment ends.

4. **Text Processing:**
	- **Spacing:** LaTeX treats multiple spaces or single line breaks as a single space; a blank line indicates a new paragraph.
	- **Sentences:** LaTeX automatically adjusts spacing after punctuation marks like periods, though specific commands may be needed if a period follows a capital letter to prevent incorrect spacing.
	- **Hyphens & Dashes:** The hyphen (-), En-dash (--), Minus sign (in math mode), and Em-dash (---).   
5. **Packages:** Users can extend LaTeX's capabilities by loading packages (files ending in `.sty`) in the preamble.
6. **Margins:** Page layout dimensions, such as text width and margins, can be customized using commands like `\setlength`.

# Font
## Font Styles and Sizes
Instead of using underlining for emphasis, LaTeX encourages changing fonts.
- **Emphasis:** Use the command `\emph{content}` to emphasize text (usually italicized) .
- **Font Sizes:**
```tex
\tiny           % Very small
\scriptsize
\footnotesize
\small
\normalsize     % Standard size
\large
\Large
\LARGE
\huge
\Huge           % Very large
```
- **Font Styles:** 
```tex
\textrm{text}   % Roman (serif)
\textsf{text}   % Sans Serif
\texttt{text}   % Typewriter (monospaced)

\textup{text}   % Upright
\textit{text}   % Italic
\textsl{text}   % Slanted
\textsc{text}   % Small Caps

\textbf{text}   % Bold
\textmd{text}   % Medium weight
```

## Alignment and Quotation
- **Centering:** Use the `center` environment to center text .
```tex
\begin{center}
	This line is centered.
\end{center}
```
- **Quotation:**
	- `quote` environment: Used for short quotes; vertical spacing between paragraphs is larger, but there is no paragraph indentation.
	- `quotation` environment: Used for longer quotes; includes paragraph indentation.

## List Environments
LaTeX supports three main types of lists, which can be nested up to 4 levels.
- **Utnordered List:** Uses bullets or other symbols.
```tex
\begin{itemize}
	\item First item
	\item Second item
\end{itemize}
```
> _Tip:_ You can change the bullet for a specific item using `\item[symbol]`.
- **Numbered List:** Uses numbers (1, 2, 3...) or letters (a, b, c...).
```tex
\begin{enumerate}
	\item Item 1
	\item Item 2
\end{enumerate}
```
- **Description List:** Used for defining terms.
```tex
\begin{description}
	\item[Keyword] Explanation of the keyword.
\end{description}
```
- **Tabbing Environment:** Used for manual column alignment similar to a typewriter
	- `\=`: set tab stops
	- `\>`: move to the next tab.
	- `\\`: line break (no automatic line breaks)
	- `\kill`: Tab stops can be set on a line that will not be printed if that line ends with
- **Changing label**
```tex
\item[$\SymboName$]
\renewcommand{\labelitemi}{$\SymbolName$}
```

## Boxes
LaTeX treats every character as a box. You can create specific boxes to hold text or drawings.
- **Paragraph Boxes:** Use `\parbox` or the `minipage` environment to create a block of text with a specific width.
```tex
\parbox[position]{width}{content}
```
- **Rule Boxes:** Use `\rule` to draw black boxes or lines.
```tex
\rule{width}{height}
```

## Tables
```
\begin{tabular}{|c|l|r|} \hline
	Col 1 (Center) & Col 2 (Left) & Col 3 (Right) \\ \hline
	Data 1         & Data 2       & Data 3        \\ \hline
\end{tabular}
```
- `c`, `l`, `r`: Column alignment (center, left, right).
- `|`: Creates vertical lines.
- `\hline`: Creates horizontal lines.
- `&`: Separates columns.
- `\\`: Ends the row (starts a new line).