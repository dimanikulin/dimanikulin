Let describe how it was before current implementation. 
Firstly it was kept at file system level inside of the Photo Album. 
Each folder in the Photo Album could keep two files: “folderDescription.json” and “description.csv”. 
“FolderDescription.json” kept information about all the files under a folder that was common. 
For example it could be device id that was the same for all multimedia files.   “FolderDescription.json” structure was:
</br>
```json
{
"deviceId":"",
"tags":"",
"people": "",
"place":"",
"event":"" 
}
```

“folderDescription.json” example:
```json
{
"deviceId":"3",
"tags":"At home, with a family",
"people": "3,6,8",
"place":"3,4",
"event":"45"
}
```

&nbsp;&nbsp;&nbsp; Description.csv has been used to keep information about files under a folder for cases if some multimedia files had different internal metadata. 
“description.csv” structure was:
</br>
&nbsp;&nbsp;&nbsp; Name,Place,People,Device,WhoTook,Description,Scaner
</br>
&nbsp;&nbsp;&nbsp; So the FVA software created or updated these files during import new files to photo album. </br> 
&nbsp;&nbsp;&nbsp; Keeping the internal metadata in this approach did not give good flexibility and maintainability. 
So adding one column in “folderDescription.json” or “description.csv” could cause whole photo album file system structure to update.
</br> 
&nbsp;&nbsp;&nbsp; So it was decided to move all “folderDescription.json” and “description.csv” to SQLlite database. 
The scheme has been created to keep the same information as “folderDescription.json” and “description.csv” did keep.
The FVA software created SQL updates to DB during import new files to photo album and all those SQL updates were kept to create SQL at any time.
</br>
&nbsp;&nbsp;&nbsp; Again keeping the internal metadata in this approach did not give good flexibility and maintainability. 
So merging one folder in photo album to another caused significant change of SQL updates.
</br>
&nbsp;&nbsp;&nbsp; So it was decided to move all information in one CSV file.
That internal metadata file does not keep information in which folder a file is kept. 
So merging one folder in photo album to another does not cause an issue.
Still the duplication of information takes place because for all files in one folder common information is just copied.

# Definitions, Acronyms, Abbreviations
| # | Abbreviation or Acronym | Definition     |
| - | ------------------------|:--------------:|
| 1 | [Dictionary](https://en.wikibooks.org/wiki/A-level_Computing/AQA/Paper_1/Fundamentals_of_data_structures/Dictionaries)|A dictionary is a general-purpose data structure for storing a group of objects. A dictionary has a set of keys and each key has a single associated value. When presented with a key, the dictionary will return the associated value. |
| 2 | [JSON](https://www.json.org/json-en.html)| JSON (JavaScript Object Notation) is a lightweight data-interchange format.|
