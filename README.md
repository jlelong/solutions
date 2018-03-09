# Solutions

This a LaTeX package to typeset exercises and their solutions.

## Typical usage

Just include the package as with any other package.

```tex
\usepackage[options]{solutions}
```

where `options` can be any of the following

- `nosol`: No solution is include.

- `inline`: The solution to a question is printed right after it.

- `after`: The answers to an entire exercise are printed right after the exercise.

- `separate`: The answers of the exercises are printed at the end of the document. If you want them to start on top of a new page, just add `\pagebreak` right before `\end{document}`.

## Customizing the layout

Here is a list of `tex` variables, which can be redefined with `\renewcommand` to modify the layout

- `\solutionsinlinename`: The title of the solution environment in `inline` mode.  
    Default value is `{\bf Solution.}\space`.

- `\solutionsinlinefont`: The font used to typeset solutions in `inline` mode.  
    Default value is `\small \itshape`.

- `\solutionsinlineendsymbol`: The symbol printed after each solution in `inline` mode.  
    Default value is `$\blacktriangle$`

- `\solutionsanswerenvname`: The title of the solution of each exercise in `after` or `separate` modes.  
    Default value is `Corrig\'e de l'exercice`.

- `\solutionsexercisename`: The title of the exercise environment.  
    Default value is `Exercice`.
