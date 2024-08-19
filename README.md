# Modular Document in LaTeX

[![made-with-latex](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/)
[![Compilation_Test](https://github.com/R0mb0/Modular_Document_in_LaTeX/actions/workflows/Compilation_Test.yml/badge.svg)](https://github.com/R0mb0/Modular_Document_in_LaTeX/actions/workflows/Compilation_Test.yml)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/2c5a717e727f46148a54f2b63131da49)](https://app.codacy.com/gh/R0mb0/Modular_Document_in_LaTeX/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)

## How to add modules (or parts)

1. Write the modules inside `modules.tex` as a new command.
2. On `Modular_document.tex` insert the modules quantity.
  	```
  	%-Where insert the number of modules----------------------------------------------------------------------------------
  	\setcounter{NModules}{3}
  	%---------------------------------------------------------------------------------------------------------------------
  	```
3. Link the modules in this section to creating the buttons for activate/deactivate modules.
   ```
   %-Line where insert buttons ------------------------------------------------------------------------------------------
		\arabic{TEMP}. \button{FModule}{\arabic{LI}} \button{SModule}{\arabic{LI}} \button{TModule}{\arabic{LI}}
    %---------------------------------------------------------------------------------------------------------------------
   ```
4. Change page header at this point
   ```
   \begin{minipage}{0.9\textwidth}
		\begin{tabularx}{\textwidth}{XX}
			{
			\raggedright
			\includegraphics[scale=0.015]{Lorem_Ipsum_Logo.jpg}
			}&{
			\vspace*{-2cm}
			\raggedleft
			%-Place where insert the header ------------------------------------------------------------------------------------------
			-Some informations here-
			%--------------------------------------------------------------------------------------------------------------------------
			}
		\end{tabularx}
	\end{minipage}
   ```
5. Add modules here to generating the document body
      ```
      %-Line where insert modules-------------------------------------------------------------------------------------------
	  \def\modules{{"\module{FModule}{\arabic{LI}}{\FModule}",
					"\module{SModule}{\arabic{LI}}{\SModule}",
					"\module{TModule}{\arabic{LI}}{\TModule}"
					}}
      %---------------------------------------------------------------------------------------------------------------------
      ```

---
# License
Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
