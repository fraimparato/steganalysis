# Create a new section in the report

1. Create a folder named "```NN_ChapterName```" in "```report/sections```"

2. Create the file in the "```report/sections/NN_ChapterName```" folder and name
it "```NN_ChapterName.tex```", where "```NN```" is the section number and
"```ChapterName```" the name of the section (or a meaningful abbreviation);

3. Copy the content of "```template.tex```" and paste it in your file;

4. In "```report/```" open "```main.tex```" and write the following line:
    
    ```
    \subfile{NN_ChapterName}
    ```