# Modular Document in LaTeX

[![made-with-latex](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/)
[![Compilation_Test](https://github.com/R0mb0/Modular_Document_in_LaTeX/actions/workflows/Compilation_Test.yml/badge.svg)](https://github.com/R0mb0/Modular_Document_in_LaTeX/actions/workflows/Compilation_Test.yml)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/2c5a717e727f46148a54f2b63131da49)](https://app.codacy.com/gh/R0mb0/Modular_Document_in_LaTeX/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)

## How to add modules (or parts) and personalize the demo document

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

## How to personalize this document online for free

1. Fork this repository by pressing the second button at the top right.
2. Rename the repository as you want and change the description then Fork it!
3. ⚠️ You have to activate "Actions" on your repo; go to "Actions", click on "I
 understand my workflows, go ahead and enable them" ⚠️
4. Upload your image using GitHub into "Modular_document\Images".
    1. Access the folder from main page.
    2. "Add file" -> "Upload files" -> drag and drop your images here.
    3. At the end, "Commit changes".
5. Access the LaTeX documents into "Modular_document".
    1. Once in the folder click on the file to personalize.
    2. Now click on "Edit this file" (the pencil on top right).
    3. Change whatever you want using comments as guide and the documentation (remember to change
 old images names).
    4. Now "Commit changes"!
6. Wait 2 minutes, got to "Actions" -> "Compile" -> click on the last one
 (look at the date on right) -> scroll down the page and click on
 "artifact file".  
7. Done! now you have your document.

---
# License
Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
