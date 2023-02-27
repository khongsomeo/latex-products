# (Unofficial) report template for HCMUS.

- Overleaf template: https://www.overleaf.com/latex/templates/hcmus-report-template/zyrhmsxynwqs

- These templates would work (best) in TexStudio or Overleaf. However, `textlive` does **not** install full LaTeX packages. In order to render some packages (e.g. `algorithm`) offline, you **must** install the `texlive-full` package (which is around 5GB!). Therefore we'd recommend you using Overleaf for the best experience. 

## Additional note

### Vietnamese code listing
`listing` package (aka `lstlisting` environment) does **not** support Vietnamese characters. To enable Vietnamese for code listing, follow these **steps**[^1]:

1. Using `listingsutf` package
2. Define a new command in `main.tex`:

	```latex
	\newcommand{\vietnameselst}{
		\lstset{literate=%
		% Vần a
			{á}{{\'a}}1
			{à}{{\`a}}1
			{ạ}{{\d a}}1
			{ả}{{\h a}}1
			{ã}{{\~ a}}1
			%
			{Á}{{\'A}}1
			{À}{{\`A}}1
			{Ạ}{{\d A}}1
			{Ả}{{\h A}}1
			{Ã}{{\~ A}}1
		%
		% Vần ă
			{ă}{{\u a}}1
			{ắ}{{\'\abreve }}1
			{ằ}{{\`\abreve }}1
			{ặ}{{\d \abreve }}1
			{ẳ}{{\h \abreve }}1
			{ẵ}{{\~\abreve }}1
			%
			{Ă}{{\u A}}1
			{Ắ}{{\'\ABREVE }}1
			{Ằ}{{\`\ABREVE }}1
			{Ặ}{{\d \ABREVE }}1
			{Ẳ}{{\h \ABREVE }}1
			{Ẵ}{{\~\ABREVE }}1
		%
		% Vần â
			{â}{{\^ a}}1
			{ấ}{{\'\acircumflex }}1
			{ầ}{{\`\acircumflex }}1
			{ậ}{{\d \acircumflex }}1
			{ẩ}{{\h \acircumflex }}1
			{ẫ}{{\~\acircumflex }}1
			%
			{Â}{{\^ A}}1
			{Ấ}{{\'\ACIRCUMFLEX }}1
			{Ầ}{{\`\ACIRCUMFLEX }}1
			{Ậ}{{\d \ACIRCUMFLEX }}1
			{Ẩ}{{\h \ACIRCUMFLEX }}1
			{Ẫ}{{\~\ACIRCUMFLEX }}1
		%
		% Vần đ
			{đ}{{\dj }}1
			{Đ}{{\DJ }}1
		%
		% Vần e
			{é}{{\'e}}1
			{è}{{\`e}}1
			{ẹ}{{\d e}}1
			{ẻ}{{\h e}}1
			{ẽ}{{\~ e}}1
			%
			{É}{{\'E}}1
			{È}{{\`E}}1
			{Ẹ}{{\d E}}1
			{Ẻ}{{\h E}}1
			{Ẽ}{{\~ E}}1
		%
		% Vần ê
			{ê}{{\^e}}1
			{ế}{{\'\ecircumflex }}1
			{ề}{{\`\ecircumflex }}1
			{ệ}{{\d \ecircumflex }}1
			{ể}{{\h \ecircumflex }}1
			{ễ}{{\~\ecircumflex }}1
			%
			{Ê}{{\^E}}1
			{Ế}{{\'\ECIRCUMFLEX }}1
			{Ề}{{\`\ECIRCUMFLEX }}1
			{Ệ}{{\d \ECIRCUMFLEX }}1
			{Ể}{{\h \ECIRCUMFLEX }}1
			{Ễ}{{\~\ECIRCUMFLEX }}1
		%
		% Vần i
			{í}{{\'i}}1
			{ì}{{\`\i }}1
			{ị}{{\d i}}1
			{ỉ}{{\h i}}1
			{ĩ}{{\~\i }}1
			%
			{Í}{{\'I}}1
			{Ì}{{\`I}}1
			{Ị}{{\d I}}1
			{Ỉ}{{\h I}}1
			{Ĩ}{{\~I}}1
		%
		% Vần o
			{ó}{{\'o}}1
			{ò}{{\`o}}1
			{ọ}{{\d o}}1
			{ỏ}{{\h o}}1
			{õ}{{\~o}}1
			%
			{Ó}{{\'O}}1
			{Ò}{{\`O}}1
			{Ọ}{{\d O}}1
			{Ỏ}{{\h O}}1
			{Õ}{{\~O}}1
		%
		% Vần ô
			{ô}{{\^o}}1
			{ố}{{\'\ocircumflex }}1
			{ồ}{{\`\ocircumflex }}1
			{ộ}{{\d \ocircumflex }}1
			{ổ}{{\h \ocircumflex }}1
			{ỗ}{{\~\ocircumflex }}1
			%
			{Ô}{{\^O}}1
			{Ố}{{\'\OCIRCUMFLEX }}1
			{Ồ}{{\`\OCIRCUMFLEX }}1
			{Ộ}{{\d \OCIRCUMFLEX }}1
			{Ổ}{{\h \OCIRCUMFLEX }}1
			{Ỗ}{{\~\OCIRCUMFLEX }}1
		%
		% Vần ơ
			{ơ}{{\ohorn }}1
			{ớ}{{\'\ohorn }}1
			{ờ}{{\`\ohorn }}1
			{ợ}{{\d \ohorn }}1
			{ở}{{\h \ohorn }}1
			{ỡ}{{\~\ohorn }}1
			%
			{Ơ}{{\OHORN }}1
			{Ớ}{{\'\OHORN }}1
			{Ờ}{{\`\OHORN }}1
			{Ợ}{{\d \OHORN }}1
			{Ở}{{\h \OHORN }}1
			{Ỡ}{{\~\OHORN }}1
		%
		% Vần u
			{ú}{{\'u}}1
			{ù}{{\`u}}1
			{ụ}{{\d u}}1
			{ủ}{{\h u}}1
			{ũ}{{\~u}}1
			%
			{Ú}{{\'U}}1
			{Ù}{{\`U}}1
			{Ụ}{{\d U}}1
			{Ủ}{{\h U}}1
			{Ũ}{{\~U}}1
		%
		% Vần ư
			{ư}{{\uhorn }}1
			{ứ}{{\'\uhorn }}1
			{ừ}{{\`\uhorn }}1
			{ự}{{\d \uhorn }}1
			{ử}{{\h \uhorn }}1
			{ữ}{{\~\uhorn }}1
			%
			{Ư}{{\UHORN }}1
			{Ứ}{{\'\UHORN }}1
			{Ừ}{{\`\UHORN }}1
			{Ự}{{\d \UHORN }}1
			{Ử}{{\h \UHORN }}1
			{Ữ}{{\~\UHORN }}1
		%
		% Vần y
			{ý}{{\'y}}1
			{ỳ}{{\`y}}1
			{ỵ}{{\d y}}1
			{ỷ}{{\h y}}1
			{ỹ}{{\~y}}1
			%
			{Ý}{{\'Y}}1
			{Ỳ}{{\`Y}}1
			{Ỵ}{{\d Y}}1
			{Ỷ}{{\h Y}}1
			{Ỹ}{{\~Y}}1
		}
	}
	```

3. Using command `\vietnameselst` **before** the code block.
4. Replace code blocks with Vietnamese to `\lstinputlisting[language]{filename}`.

The code block after step 4 looks something like this:
```latex
\vietnameselst
\lstinputlisting{filename}
```

Credit: [thiminhnhut/latex](https://github.com/thiminhnhut/latex/blob/master/tips/listings/tiengviet-trong-listings/tiengviet-trong-listings.tex)

- [^1]: Please remember that these are **steps**, not **options**.
