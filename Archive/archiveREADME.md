# GPT Dialog Archives
### Overview
Dialogs are to be archived into the directory that corresponds to the associated model. 

there are two options for storing logs. 

There's the `singlefile` and `directory` method, both work. 

### Directory Method
The entirety of the conversation is contained and represented as a single directory. Directory name can be one of following:
 
+ Appropriate descriptive title
+ ISOFormat Timestamp of the response
+ Given an autoincremented value 
+ **All the filenames should also include -
  * Response index in the conversation
  * Identity (U for User, GPT for bot)
  * type of response (prompt, normal, final, error)
  

In each file, there should be achecksum of the file's encoded contents and a master passphrase. This should be checked.
After the first line containing the checksum, a shebang denoted by a a line of repeating non alpha characters. The next newline then marks the start of the response string.
