# Create a new section in the report

1. Create the file in the "```report/sections/```" folder and name it
"```NN_ChapterName.tex```", where "```NN```" is the section number and
"```ChapterName```" the name of the section (or a meaningful abbreviation);

2. Copy the content of "```template.tex```" and paste it in your file;

3. In "```report/```" open "```main.tex```" and write the following lines:
    
    ```
    \subfile{NN_ChapterName}
    ```