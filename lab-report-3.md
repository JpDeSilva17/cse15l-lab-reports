# Lab Report 3

I chose to focus on the grep command for my third lab report. To get a general sense of its use and versatility, I first chose to enter ```man grep```
into the command line to read up on the documentation provided by the system. 

```
DESCRIPTION
       grep searches the named input FILEs (or standard input if no files are named, or if a single hyphen-minus (-) is given as file name) for 
       lines containing a match to the given PATTERN.  By default, grep prints the matching lines.
```

This was helpul, but in order to conceptualize it better I asked ChatGPT to explain it to me like I'm five. 

This was its response: 
```grep``` is like a magic detective that helps you find a specific word or phrase in a really big book. 
You tell the detective what word you're looking for, and the detective looks through the whole book to find any places where that word is written. 
Then the detective tells you where the word is in the book so you can find it easily. It's really helpful when you don't want to read the whole book, 
but just want to find a specific thing in it.

Now that we have a much better understanding of ```grep``` we can begin testing different modifications of the command on files in the ```technical```
directory. I chose to use the same files that were provided for ```stringsearch-data``` in our skill demonstration since I was already familiar with them.

I found all of the commands I used from the official ```grep``` documentation on [gnu.org](https://www.gnu.org/software/grep/manual/grep.html).



# grep -c


```grep -c``` is a command that is used to count the number of lines that a particular word or pattern appears in within a file. This can be useful in
situations where you're only interested in the amount of times that a certain word appears in a file without needing to know the actual content of those 
lines.



The following ```grep -c``` command was used to search the amount of lines that the word "law" appeared in the Survey.txt file in the technical directory:

```
[cs15lsp23lw@ieng6-201]:stringsearch:472$ grep -c "law" stringsearch-data/technical/government/Media/Survey.txt
28
```



The following ```grep -c``` command was used to search the amount of lines that the word "and" appeared in the Survey.txt file in the technical directory:

```
[cs15lsp23lw@ieng6-201]:stringsearch:470$ grep -c "and" stringsearch-data/technical/government/Media/Survey.txt
30
```


# grep -l

The ```grep -l```  command is used to display the names of files that contain a certain pattern or word. This can be useful in situations where you are 
trying to quickly identify which files contain a certain pattern or word without having to open each file and manually search for it.



The following ```grep -l``` command is used to search the files where the word "space" exists within the 
```stringsearch-data/technical/government/Media/``` directory: 

```
[cs15lsp23lw@ieng6-201]:stringsearch:484$ grep -l "space" stringsearch-data/technical/government/Media/*.txt
stringsearch-data/technical/government/Media/5_Legal_Groups.txt
stringsearch-data/technical/government/Media/Advocate_for_Poor.txt
stringsearch-data/technical/government/Media/CommercialAppealMemphis2.txt
stringsearch-data/technical/government/Media/Crains_New_York_Business.txt
stringsearch-data/technical/government/Media/Nonprofit_Buys.txt
stringsearch-data/technical/government/Media/Owning_a_Piece.txt
stringsearch-data/technical/government/Media/Targeting_Domestic_Violence.txt
stringsearch-data/technical/government/Media/defend_yourself.txt
stringsearch-data/technical/government/Media/not_accessible_to_disabled.txt
```



The following ```grep -l``` command is used to search the files where the word "machine" exists within the 
```stringsearch-data/technical/government/Media/``` directory: 

```
[cs15lsp23lw@ieng6-201]:stringsearch:486$ grep -l "machine" stringsearch-data/technical/government/Media/*.txt
stringsearch-data/technical/government/Media/Free_Legal_Assistance.txt
stringsearch-data/technical/government/Media/Pro-bono_road_show.txt
stringsearch-data/technical/government/Media/Terrorist_Attack.txt
```


# grep -rn


The ```grep -rn``` command is used to recursively search through all of the subdirectories under a directory for the file name and the line number 
and contents of a particular pattern. the ```r``` is for recursive while the ```n``` is for number. This is useful, because it adds a more detailed element to the previous command whereas ```grep -l``` only prints out the file in which a pattern exists, ```grep -rn``` prints out the file, the line number, and the line in which the pattern exists. 



The following ```grep -rn``` command is used to recursively search through the subdirectories of ```technical/``` in which the word "machine" exists, and proceeds to display the file name, and the line number/contents. 

```
grep -rn [cs15lsp23lw@ieng6-201]:stringsearch:487$ grep -rn  "machine" stringsearch-data/technical/government/Media/*.txt
stringsearch-data/technical/government/Media/Free_Legal_Assistance.txt:82:use the two machines.
stringsearch-data/technical/government/Media/Pro-bono_road_show.txt:17:Pecina, 38, a machine operator at Levi Strauss & Co., has
stringsearch-data/technical/government/Media/Terrorist_Attack.txt:36:Yee, at the fax machine. She had just sent the official news to the
stringsearch-data/technical/government/Media/Terrorist_Attack.txt:38:"I took the cord out of the wall from the fax machine," Mr.
```



The following ```grep -rn``` command is used to recursively search through the subdirectories of ```technical/``` in which the word "machine" exists, and proceeds to display the file name, and the line number/contents. 

```
[cs15lsp23lw@ieng6-201]:stringsearch:488$ grep -rn  "technical" stringsearch-data/technical/government/Media/*.txt
stringsearch-data/technical/government/Media/Abuse_penalties.txt:16:after a hearing or through a technical violation or plea.
stringsearch-data/technical/government/Media/New_Online_Resources.txt:27:complex," she added, "but it really allows nontechnical people like
```


# grep -o 


The ```grep -o``` command is used to display only the matched pattern or word and its corresponding file, rather than the entire contents of the line. This is useful for when you're  searching for a specific pattern or word within a file, and you only want to see the exact matches without any extra text.



The following is a ```grep -o``` command that searches for exact instances of the word "technical" within the 
```stringsearch-data/technical/government/Media/*.txt``` directory:

```
[cs15lsp23lw@ieng6-201]:stringsearch:490$ grep -o  "technical" stringsearch-data/technical/government/Media/*.txt
stringsearch-data/technical/government/Media/Abuse_penalties.txt:technical
stringsearch-data/technical/government/Media/New_Online_Resources.txt:technical
```



The following is a ```grep -o``` command that searches for exact instances of the word "machine" within the 
```stringsearch-data/technical/government/Media/*.txt``` directory:

```
[cs15lsp23lw@ieng6-201]:stringsearch:491$ grep -o  "machine" stringsearch-data/technical/government/Media/*.txt
stringsearch-data/technical/government/Media/Free_Legal_Assistance.txt:machine
stringsearch-data/technical/government/Media/Pro-bono_road_show.txt:machine
stringsearch-data/technical/government/Media/Terrorist_Attack.txt:machine
stringsearch-data/technical/government/Media/Terrorist_Attack.txt:machine
```
