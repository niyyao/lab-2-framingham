# AI Usage Log — Lab 2

Model used: Claude (Anthropic)

## Interaction 1: Finding a working data-load URL

I used Claude to help find a working URL to load the dataset from. In the Framingham Heart Study there was only an example link: https://github.com/GauravPadawe/Framingham-Heart-Study/blob/master/framingham.csv

I asked Claude why that link wouldn't work directly in pd.read_csv(). Claude explained that this is a GitHub webpage (HTML), not the raw file, and that GitHub serves raw file bytes at a different domain, raw.githubusercontent.com, instead of github.com/.../blob/.... Claude gave me the corresponding raw URL: https://raw.githubusercontent.com/GauravPadawe/Framingham-Heart-Study/master/framingham.csv

I verified this worked by running pd.read_csv(url) followed by fram.head(), which returned a populated table with the expected columns (male, age, currentSmoker, TenYearCHD, etc.) instead of an error, confirming the data loaded correctly from its original source.

## Interaction 2: Fixing a SyntaxError in the interpretation cell

I used Claude to help fix an error. After running my interpretation cell, I got:

Cell In[6], line 1
    The steady incease of CHD prevalence across age groups shows that people become more at risk of CHD as they grow older...
    ^
SyntaxError: invalid syntax

I asked Claude where the SyntaxError was coming from before asking how to fix it. Claude explained that two of my cells ([5] and [6]) were still set to "Code" type instead of "Markdown," so Jupyter was trying to run my heading and paragraph as Python code. The fix was to select each cell, press Esc then m to convert it to Markdown, then Shift+Enter to re-run it. I checked to see if it worked by restarting the kernel and running all cells, and it did — the whole notebook ran top-to-bottom with no errors anywhere.
