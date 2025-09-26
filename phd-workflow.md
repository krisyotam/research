Directory structure:

```
.
├── papers
│   ├── Title - Author.pdf
│   └── Title - Author.pdf
├── notes
│   ├── 2022-04-10
│   │   ├── note.tex
│   │   └── note.xoj
│   ├── 2022-04-11
│   │   ├── note.tex
│   │   └── note.xoj
│   ├── ...
│   ├── master.tex
│   ├── preamble.tex
│   ├── references.tex
│   ├── symbols.tex
│   └── theorems.tex
└── scripts
    ├── ...
    ├── shortcut.sh
    └── template.xoj
```

Sxhkd config:
```
# ~/.config/sxhkd/sxhkdrc 

alt + {a-z}
    bash ~/phd/scripts/shortcut.sh {a-z}
```

This way, any combination of <kbd>Alt</kbd> + <kbd>$KEY</kbd> calls `scripts/shortcut.sh $KEY`.
This is a bash script with the following shortcuts:

* <kbd>Alt</kbd> + <kbd>F</kbd> copies a reference to the currently opened pdf.
* <kbd>Alt</kbd> + <kbd>N</kbd> opens the note of today.
* <kbd>Alt</kbd> + <kbd>O</kbd> opens the compiled version of my notes.
* <kbd>Alt</kbd> + <kbd>P</kbd> allows me to fuzzy search a paper.
* <kbd>Alt</kbd> + <kbd>R</kbd> opens my file browser in my phd directory.
* <kbd>Alt</kbd> + <kbd>X</kbd> opens today's handwritten notes and if not existing copies the template to today's directory and opens it .

You'll have to edit `shortcut` a bit to make this work on your system.
