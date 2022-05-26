# HOW TO

## Index

- [Create a new section in the report](#create-a-new-section-in-the-report)
- [Add a reference](#add-a-reference)
- [General advices](#general-advices)

### Create a new section in the report

1. Create a folder named `NN_ChapterName` in `report/sections`

1. Create the file in the `report/sections/NN_ChapterName` folder and name
it `NN_ChapterName.tex`, where `NN` is the section number and
`ChapterName` the name of the section (or a meaningful abbreviation) 

    * No SPACES
    * **CamelCase** for the chapter name


        ```
        report
        |__sections
                |__00_Example
                |   |__00_Example.tex
                |
                |__01_ImageHiding
                |    |__01_ImageHiding.tex
                |
                |__02_AudioHiding
                    |__02_AudioHiding

            ...
                
        ```
1. Use the default template: Copy the content of ```template.tex``` and paste it
in your file

1. Open ```report\main.tex``` and write the following line (you have to substitute
the general name used in the example with your file and folder's name):
        
    ```
    ...

    \subfile{sections/NN_ChapterName/NN_ChapterName.tex}
    
    ...    
    ```

### Add a reference

Whenever a reference to a book or an article is made, it is needed to update the
bibliography. You have to add the work in ```references.bib``` in the
```report/``` folder with the following syntax:

- for a book:

    ```
    @book{book_code,
        author = "Surname, Name",
        title = "Book Title",
        year = "2022",
        publisher = "Publisher name",
        editor = "Editor name",
        ...
    }
    ```
    note that you can change the order of fields and also that not all the
    fields are always needed;

- for a scientific paper:

    ```
    @report{report_code,
        author = "Surname, Name",
        title = "Report Title",
        year = "2022",
    }
    ```

Then, to cite the article/book, in the ```.tex``` file you're writing, you have
to add the following:

```
\cite{code_you_need}
```

### General advices

- In order to have a more clean code, go to a new line whenever you reach the
80th column (80th character on the current line) and when you reach a full stop
- Write meaningful and frequent commits

```
    ___________________
    |                 |
    |    __     __    |   ________________
    |   |  |   |  |   |   | Leggi        |
    |   |__|   |__|   |   | e non fare il|
    |                 |   |  furbetto    |
    |        __       |   |______________|
    |       |__|      |        __/
    |_________________|
            /|\
             |
            / \

```