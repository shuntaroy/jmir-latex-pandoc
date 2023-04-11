# JMIR unofficial LaTeX template for Pandoc's Word conversion

This gives a LaTeX template for the JMIR journal, where only the Word template is officially available.
Although this LaTeX template cannot replace the official Word template, it can be used to convert a manuscript to Word format.

## Usage

First, draft your manuscript with `./tex/main.tex` as the main file in your favourite way (local latex env, or Overleaf, etc.). 

After you finishing the draft, convert the manuscript to Word format with the following commands:

```sh
$ pandoc -C --bibliography jmir.bib --csl ./word/american-medical-association.csl --reference-doc ./word/custom-reference.docx main.tex -t docx -o ./word/main.docx
```

You will obtain `main.docx` under the `./tex` folder.

Finally, please manually fix the `main.docx` to follow the `./word/InstructionsForAuthorsOfJMIR.docx`.

Some of the manual fixes would be:
- Add table/figure labels
- Modify the table format and style
- Reformat the references

## Notes

The LaTeX template is designed to be looking similar enough to the official Word template, meaning it's not a perfect replication.
Please use it only for the drafting.