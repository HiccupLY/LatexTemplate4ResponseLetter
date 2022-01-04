# Response Letters
Latex template to quickly write response letters to review comments. 

Based on @mschroen's [review_response_letter](https://github.com/mschroen/review_response_letter). 

## Example
Use the example `reply.tex`. Please ensure the class file `ar2rc.cls` and the style file `commands.sty` are in the same directory.

<img alt="Screenshot of the output PDF of a Author Response Letter to Review Comments" src="https://cloud.githubusercontent.com/assets/7942719/26349939/c9889c00-3fb1-11e7-91c6-908012e2797e.png" style="max-width: 100%" />

In the commands, several function are listed as follows:
\reviewersection : define the new reviewer environment with index added.
\totalcomment : define the initial comment.(optional)
\generalresponse : define the reply of the initial comment.(optional)
\point : define the new argue point of the specific reviewer(\reviewersection).
\reply : define the reply part.
\textupdate : define the updated text.
\textdel : define the deleted text.


```
\reviewersection
\label{reviewer.1}

\begin{totalcomment}
    \lipsum[1-1]
\end{totalcomment}

% Point one description 
\begin{point} \label{pt:1.1}
    \lipsum[1-1]
\end{point}

% Our reply
\begin{reply}
    \lipsum[1-1]

	begin{quote}
		\textupdate{This is a demo.}
		\textdel{This is a demo.}

		The cat in the box is \DIFdelbegin \DIFdel{dead}\DIFdelend \DIFaddbegin \DIFadd{alive}\DIFaddend . 
	\end{quote}
\end{reply}
```

Then run `pdflatex myletter.tex` to make `myletter.pdf`, or typeset with any TeX front-end program.
