# LaTeX

## Bibliography: technical aspects 
This project uses the package biblatex to handle the bibliography, therefore it needs biber as the bibliography tool, instead of bibtex. Additionally, it is suggested that all bib entries include a DOI and/or URL.

## Best practices

1. Use `\colon` instead of `:` for defining functions.

2. Use `\mid` for sets or group presentations. For example, `\set{a \in A \mid a=b}` is superior to `\set{a \in A | a=b}`.

3. Leave space around most operators. For example, `f \colon X \to Y` is superior to `f:X\to Y`. Possible exceptions are guided by readability, for example:

	```latex
	\begin{equation}
	   \sum_{i=1}^n = \frac{n(n+1)}{2}.
	\end{equation}
	```

4. No punctuation inside math mode. Use `$a+b$,` instead of `$a+b,$`.

5. No line breaks in the middle of sentences.

6. Use line breaks at the end of each sentences.

7. No double blank spaces or trailing blank spaces.

8. Use tab instead of blank spaces for indentation.

9. All named environments with the possible exception of `document` should be tabbed. For example,

	```latex
	\begin{lemma*}
	   Statement.
	\end{lemma*}
	```

10. Do not use `$$...$$` for display equations; instead, use one of the environments in the AMS display equation family or
	
	```latex
	\[
	Content,
	\]
	```
which is not considered an environment, so it is not tabbed.

11. Leave a blank line before and after most environments. Possible exceptions are AMS display equation family.

12. Leave a blank line before and after sections and subsections.

13. Unless a there is a good reason not to, use `\dots` instead of either `\ldots` or `\cdots` or others. The `amsmath` package uses nearby operators to choose the right type of dots for `\dots`.

14. Line breaks inside display equations should be minimized. When breaking keep a binary operator on the top row.

	```latex
	\[
	Long left hand side =
	Long right hand side
	\]
	```

15. Use `\set{...}` instead of `\{...\}`. Recall that parenthesis can be increased in size using `\set[\big]{...}` and similar variations.

16. Use `\defn{...}` for definitions of new concepts, even inside a definition environment, instead of `\textbf{...}`, `\textit{...}`, or `\emph{...}`.

17. Use `\cref{...}` for all cross-references instead of `\ref{...}` or `\autoref{...}`.

18. Place `\label{...}` immediately following the environment declaration on the same line with no intervening space, e.g., `\begin{theorem}\label{st:main}`.

19. Standardize label prefixes using the following taxonomy:
	* `st:` for statements (theorems, lemmas, propositions, corollaries).
	* `d:` for definitions.
	* `eq:` for equations and display math environments.
	* `ex` for examples.
