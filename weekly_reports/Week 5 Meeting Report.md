---
title: Week 5 Meeting Report
tags: Templates, Report
description: Weekly Meeting Report
---

# Week 5 - Meeting Report

Time: 18/10/2021 Mon 12:00-12:30

# Week 4 - Recap

previous week we went through:

* could start researching about ANTLR, JVM etc.
* could experiment with the small Pascal grammar example
* currently no need to go deep of DFA, NFA, LL(*) parsing algo etc.
    * but might worth constrast the difference between top-down and bottom-up costruction methods later in dissertation.
* currently further code transformation might not be needed

# Week 4 - Progress

* Brief reading Pascal tutorial (tutorialspoint - Pascal quick guide)
* Write very simple example Pascal grammar
    * things like HelloWorld
* Research about ANTLR and AST etc.
* Revised PL coursework driver class structure etc.

# Questions

## Project-Related Questions

> Pascal to JVM compiler
> 
> The aim is to design and implement a compiler for the classic programming language Pascal (or another language), using Java Virtual Machine code as the target language. If time permits, language extensions can be explored.
> 
> Ideally the student will have taken PL(H). This project is an opportunity to put the concepts and techniques of that course into practice, as well as gaining an in-depth knowledge of the Java Virtual Machine.


1. I've found the implemented Pascal grammar (haven't went thorugh it yet) in ANLTR github repo, what would be the best practice to implement it then?

* based on understanding first implment in person while refering it
* or copy the basic lexer rules then implement the rest part

2. What would be the best practice to define the grammar? 

* ![](https://i.imgur.com/HPCEqvA.png) like implement basic block first then go deep?
* My first try - I've found myself lost, as first choosing various example programs as the starting point

3. When defining the grammar, what would be the best practice to distignuish the reserved word and identifier?

4. (**if have time, currently don't think these have higher priority than the extension direction of implementing other Pascal features**) Could '*encapsulate the implemented compiler*' be an extension of this project? (usage/deployment extension)

* i.e. develop an command line tool for usage, then deployed both on NPM and dockerhub
    * consider develop IDE plugin seems little bit tricky to handle, and there are various NodeJs tutorials of how to make command line tools.

5. (**if have time, same as above**) Apart from the CMD tool, I'm also thinking about utilising the AST generated from ANTLR

* like
    * generating the AST visualisation files (when user request in command line)
    * static analysis the source Pascal program (might be lots work to do) etc.

6. Is that right in the visitor patterns, when we start at a node, we would try to iterate all its children no matter it matches or not?

* i.e. for loop into all the branches given in grammar, which seems not that efficient... shall we try to optimise it if possible?



# Blockers

--

# This week Plan (After Meeting)

* Orgnize minutes of this week
* Should finish looking Pascal syntax
    * quick looking website resouces
    * looking book to reinforce the understanding
* continue looking in the suggested book (*Programming language processors in Java*)


---

# Week 5 - Meeting Minutes

would be organized after meeting... 

## 3rd Meeting: 18/10/21 - Mon

time: 12:00 - 12:30

## Things Agreed & Acknowledged

1. Consider modifying the structure of comment lexer rules

* do not put it inside the parser rules, best practice: handle to skip channel

2. Parser rule of String (QUOTE STRING QUOTE) might be changed to something like (`'`|STRING)

3. Reference the implemented Pascal grammar of ANTLR repo and the suggested book

4. How to process the built-in methods?

* no need to include all the built-in method identifier as the lexer rules, just left `ID()`， as assumed user-defined method would override the same identifier
    * need way to identify between them later on(searching order etc)

5. Reserved word should come first before any other lexer rules

* consider ANTLR features, to handle the ambiguity, would choosing the top first alternative (or choose the rule which match the longgest string as possible).

## Before Next Meeting

* Organize previous meeting minutes
* Should finish looking Pascal syntax
    * quick looking website resouces
    * looking book to reinforce the understanding
* continue looking in the suggested book (*Programming language processors in Java*)