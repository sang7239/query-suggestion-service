# query-suggestion-service


## Overview

![alt text](/files/wiggle_suggestions.png)

### Trie Implementation
I implementing my trie using trienode, each of which contains its own list of children. Each trie node is assigned its letter value and whether it is the end of a word.

First method is "Add Title" method which takes in a string 'word' as parameter and adds the word to the trie by traversing down its children.

Second method is "GetWordsWithPrefix" method which also takes in string prefix parameter and traverses the trie to retrieve search results sharing the same prefix. 

### Pre-processing dictionary words

Using the Console App project, I used both the Streamreader and Streamwriter read textfile and output a new textfile containing only the desired titles [a-z], [A-Z], and underscores. Using the replace method, I replaced every underscore with a space and outputted a new file to be used for building my trie. 

### Implementing WebService and ajax

After the constructing the trie data structure, I implemented the webservice methods with ajax calls using jquery. In my Webservice, my method "buildTrie" reads each line of word adds to trie.

The method "GetWordsWithPrefix"  calls and returns the JSON value of the results obtained from passing in titles to trie.GetWordsWithPrefix function. 
