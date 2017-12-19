# Info206_GroupA
- Group A
- Team name: JJBS
- Team members: Bo Brandt, Sejal Popat, Jason Zhixuan Dai, Jiaxun Song

## 1. Problem statement
The project for this course is to build a smart text editor/processor that incorporates “intelligent” behaviors of modern-day text interfaces including autocomplete, flagging misspelled words and other interactive functions.  
## 2. Use cases
Like most of other text editors, the users will type in a text box as input. This input will be processed in the program. The output will be various processed text, including highlighted words when the words are not in an English dictionary, Flesch index which indicates the complexity of the input text, Markov Text which is a newly generated text that mimics the style of the users' input, etc.
## 3. Assumptions and constraints
We assume that the input comes from users' typing. The text content will be processed and display in the program. The implement of some of the key algorithms in our program may become our constraints. For instance, we need to figure out how to dynamically analyze the text input inside the GUI. Also, we need to optimize the data structure for our data storage so that it can respond fast.  
## 4. Architecture
### Structure
![picture1](https://user-images.githubusercontent.com/31323106/31590350-5dac0998-b1c3-11e7-9b28-56164db272e7.png)
The group collaboratively draw the implementation  blueprint.
### Main interface
![screen shot 2017-10-14 at 2 24 54 pm](https://user-images.githubusercontent.com/31323106/31590375-da828df2-b1c3-11e7-9b32-eb5fbc027ec2.png)
## 5. Implementation plan
### Main interface
The GUI will be designed using a python built-in library tkinter. This GUI library will provide following classes that we will use: Text, Entry, Button, Checkbutton, Scrollbar and messagebox. Although the tkinter is powerful, it does not provide a text box that can capture user’s input dynamically. So we have to inherit the text box from tkinter.Text and add new attributes and methods in order to implement our functions.  
**Jiaxun will work on this part.**
### TrieTree
TrieTree module eases the implementation of the corpus dictionary and wording functions. It includes two classes: Trie and DicTree. Trie is a data structure we will construct to hold each word we add to the dictionary. DicTree will be made up of a tree of Trie nodes and used as the dictionary of words, a reference to check if an input word is really a word in this dictionary and provides reference completion lists for any incomplete input.
![picture2](https://user-images.githubusercontent.com/31323106/31590525-8183aa8a-b1c6-11e7-8c51-7b3cb6e20c2b.png)  
**Jason worked out this part.**

### Spelling Check
Depending on the Trie data structure and TrieTree module implemented above, the system can decide if the word is an existing word in the dictionary we imported according to the isWord method in TrieTree. 
**Jason worked out this part.**

### Translation
Rely on Baidu API.  
**Jiaxun will work on this part.**
### Word Cloud
Rely on an existing module called wordcould.  
**Jiaxun will work on this part.**
### Flesch Index
Given the text input, calculate the Flesch Score by finding the total number of words, syllables, and sentences.   
**Bo will work on this part.**
### Markov Text
Given an input text, generate a new sequence of words that fit the style of the source. Style is determined by how often words occur in sequence.  
![markov](Markov.png)
## 6. Test plan
We will personally type in to test the program. In addition, we will use excerpts from different articles such as GRE reading, political news, and fairy tales, to test our functions.
## 7. Run the code
  1. Please install one more library before running the code.
  ```
    pip install wordcloud
  ```
  2. The script JJBS.py is our main program, so please run this code in terminal or in IDE.
