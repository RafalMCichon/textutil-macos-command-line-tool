# Textutil Usage Guide

`textutil` is a powerful command-line utility included with macOS that is used for converting and manipulating text files. It supports a variety of formats including plain text, Rich Text Format (RTF), Rich Text Format Directory (RTFD), HTML, Word (doc, docx), OpenDocument Text (odt), WordPerfect (wp), and Webarchive.

## Basic Usage

The general syntax for using `textutil` is as follows:

```
textutil -convert format [-output file] [-cat format] [-info] [-extension ext] [-inputencoding enc] [-outputencoding enc] file...
```

## Examples

Here are some examples of how `textutil` can be used:

1. **Convert a single file to another format:**
    ```
    textutil -convert txt Document.docx
    ```

2. **Specify the output file name:**
    ```
    textutil -convert txt -output Output.txt Document.docx
    ```

3. **Convert multiple files at once:**
    ```
    textutil -convert txt Document1.docx Document2.docx Document3.docx
    ```

4. **Concatenate files:**
    ```
    textutil -cat txt -output Output.txt Document1.txt Document2.txt
    ```

5. **Change the text encoding of a file:**
    ```
    textutil -convert txt -inputencoding ISO-8859-1 -outputencoding UTF-8 Document.txt
    ```

6. **Extract the text content from an HTML file:**
    ```
    textutil -convert txt Document.html
    ```

7. **Create a Word document from a text file:**
    ```
    textutil -convert docx Document.txt
    ```

8. **View the information of a file:**
    ```
    textutil -info Document.docx
    ```

9. **Converting to an OpenDocument Text (odt) file:**
    ```
    textutil -convert odt Document.docx
    ```

10. **Converting to a WordPerfect (wp) file:**
    ```
    textutil -convert wp Document.docx
    ```

11. **Converting to a webarchive file:**
    ```
    textutil -convert webarchive Document.html
    ```

12. **Concatenating files of different formats:**
    ```
    textutil -cat docx -output Output.docx Document.txt Document.docx
    ```

13. **Converting a file to HTML with specified text encoding:**
    ```
    textutil -convert html -outputencoding UTF-8 Document.docx
    ```

14. **Converting an RTF file to plain text:**
    ```
    textutil -convert txt Document.rtf
    ```

15. **Converting all files of a certain type in a directory:**
    ```
    textutil -convert txt *.docx
    ```

16. **Creating a Rich Text Format Directory (RTFD) file from a text file:**
    ```
    textutil -convert rtfd Document.txt
    ```

17. **Concatenating and converting files:**
    ```
    textutil -cat docx -output Combined.docx File1.txt File2.txt File3.txt
    ```

18. **Converting a Word document to a `.pdf` using `cupsfilter`:**
    ```
    textutil -convert ps Document.docx
    cupsfilter Document.ps > Document.pdf
    ```

19. **Read from standard input (`stdin`) and output to standard file:**
    ```
    echo "This is some text"

| textutil -convert rtf -stdin -output Output.rtf
    ```

20. **Output to standard output (`stdout`):**
    ```
    textutil -convert txt -stdout Document.docx
    ```

21. **Specify the text encoding for output files:**
    ```
    textutil -convert txt -encoding ISO-8859-1 Document.docx
    ```

22. **Specify the input text encoding:**
    ```
    textutil -convert docx -inputencoding ISO-8859-1 Document.txt
    ```

23. **Force the input files to be interpreted in a specific format:**
    ```
    textutil -convert txt -format docx Document.docx
    ```

24. **Specify font and size when converting plain text to rich text:**
    ```
    textutil -convert rtf -font Helvetica -fontsize 12 Document.txt
    ```

25. **Exclude specific HTML elements from the output:**
    ```
    textutil -convert txt -excludedelements "(script, style)" Document.html
    ```

Remember, in all these examples, replace `Document.docx`, `Document.html`, etc. with the actual paths to your files. All these commands are run from the terminal application.

---

## Further Information

To get more detailed information about `textutil` and its usage, you can view its manual page by typing `man textutil` in the Terminal. The manual page will provide a detailed description of how to use `textutil`, including a list of all its options and examples of its usage.

---

That's the basic guide to using `textutil`. It's a powerful tool that can be extremely useful for working with different text file formats on a macOS system. Be sure to replace the filenames and paths in the examples with those that match your actual files and directory structure.