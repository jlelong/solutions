# Solutions

This a LaTeX package to typeset exercises and their solutions.

## Typical usage

Include the package

```tex
\usepackage[options]{solutions}
```

where `options` can be any of the following

- `nosol`: No solution is include.

- `inline`: The solution to a question is printed right after it.

- `after`: The answers to an entire exercise are printed right after the exercise.

- `separate`: The answers of the exercises are printed at the end of the document. If you want them to start on top of a new page, just add `\pagebreak` right before `\end{document}`.

### Typesetting an exercise with questions

```tex
\begin{exercise}[optional title]
    Some optional introductive text.
    \begin{questions}
        \item Question 1.
            \solution{Solution to the previous question.}
        \item Question 2.
            \solution{Solution to the previous question.}
    \end{questions}
    Add some extra global information if any
    \begin{questions}[resume]
        \item Question 3.
            \solution{Solution to the previous question.}
        \item Question 4.
            \solution{Solution to the previous question.}
    \end{questions}
\end{exercise}
```

To use the `resume` option, you need to include the `enumitem` package.

### Typesetting an exercise with questions and sub questions

```tex
\begin{exercise}[optional title]
    Some optional introductive text.
    \begin{questions}
        \item Question 1.
            \solution{Solution to the previous question.}
        \item \begin{subquestions}
                \item Sub Question 1.
                    \solution{Solution to Sub Question 1.}
                \item Sub Question 2
                    \solution{Solution to  Sub Question 2.}
            \end{subquestions}
        \item Question 3.
            \solution{Solution to the previous question.}
    \end{questions}
\end{exercise}
```

It is possible to group the solutions to all sub questions in a single one

```tex
\begin{exercise}[optional title]
    Some optional introductive text.
    \begin{questions}
        \item Question 1.
            \solution{Solution to the previous question.}
        \item \begin{subquestions}
                \item Sub Question 1.
                \item Sub Question 2
            \end{subquestions}
            \solution{Global solution to Sbu Questions 1 and 2.}
        \item Question 3.
            \solution{Solution to the previous question.}
    \end{questions}
\end{exercise}
```

### Typesetting an exercise with a single question

```tex
\begin{exercise}[optional title]
    The text of the exercise.

    \solution{Solution of the exercise.}
\end{exercise}
```

## Customizing the layout

Here is a list of `tex` variables, which can be redefined with `\renewcommand` to modify the layout

- `\solutionsanswerinlinename`: The title of the solution environment in `inline` mode. Default value is `{\bf Solution.}\space`.

- `\solutionsanswerinlinefont`: The font used to typeset solutions in `inline` mode. Default value is `\small \itshape`.

- `\solutionsanswerinlineendsymbol`: The symbol printed after each solution in `inline` mode. Default value is `$\blacktriangle$`.

- `\solutionsanswerenvname`: The title of the solution of each exercise in `after` or `separate` modes. Default value is `Corrig\'e de l'exercice`.

- `\solutionsanswerfont`: The font used to typeset solutions in `after` and `separate` modes. Default value is `\small`.

- `\solutionsexercisename`: The title of the exercise environment. Default value is `Exercice`.
