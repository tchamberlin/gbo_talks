# Parsing and Manipulating Tables

How to parse tables from the internet, and how to perform basic slicing/indexing on them once they have been parsed

- [Notebook](./tables_talk.ipynb)
- [Slides](https://www.gb.nrao.edu/~tchamber/slides/tables_talk.slides.html)

This talk is presented both as a Notebook and as slides, via RISE/reveal.js

## Installation

If you want to run this notebook locally:

```
# Create a virtual environment (or similar...)
python -m venv /path/to/venv

# Install requirements
pip install -r requirements.txt

# Enable rise
jupyter-nbextension enable rise --py

# Start Jupyter Notebook server
jupyter notebook
```

You should now be able to enter the live slideshow view with `Alt+R`. For full RISE installation instructions, see https://rise.readthedocs.io/en/stable/installation.html

To render the final static version of the slides, you can use:

```
$ jupyter nbconvert ./tables_talk.ipynb --to slides
```

Or the `File -> Download as -> Reveal.js slides` context menu

## Slides

Note that all cells that you want to include in the slideshow _must_ have their slides type set to a non-blank value:

`Slide`: A "full" slide. These form the horizontal axis of the slideshow
`Sub-Slide`: Basically the same as a Slide, but will show up as `N.M`, e.g. the third Sub-Slide of Slide 5 is 5.3
`Fragment`: Appears on the current Slide or Sub-Slide, but only after navigating forward (it will fade in)
`-`: Includes the cell as a direct part of the current Slide or Sub-Slide
`Notes`: Include in the slideshow, but only in the speaker's notes (Hotkey `t`)
`<blank>`: Don't include in the slideshow

In order to set Slide Type, you will need to enable the Slides toolbar: View -> Cell Toolbar -> Slides
