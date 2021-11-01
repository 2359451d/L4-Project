---
title: Week 6 Meeting Report
tags: Templates, Report
description: Weekly Meeting Report
---

# Week 6 - Meeting Report

Time: 25/10/2021 Mon 12:00-12:30

# Week 5 - Recap

previous week we went through:

* Could reference the implemented Pascal grammar of ANTLR repo and the suggested book
    * adjust implementation starting point
* How to process the built-in methods
    * no need to include all the built-in method identifier as the lexer rules, just left `ID()`， as assumed user-defined method would override the same identifier
    * need way to identify between them later on(searching order etc)
* Reserved word should come first before any other lexer rules
    * consider ANTLR features, to handle the ambiguity, would choosing the top first alternative (or choose the rule which match the longgest string as possible).

# Week 5 - Progress

* Continue researching about ANLTR
* Start looking in the book *The Definitive ANTLR 4 Reference*
    * also gathered points for dissertation preparation

# Questions

## General Questions

1. What would be the best strategy to finish the reading of several books

* currently I've found myself in no order, even though I put focus on one book each week, when I'm confusing about something and start researching, the process would never stop and lead to low productivity
    * introduced other new concepts and research them again like a loop
    * and when I try to go back to the first confusing point, it already takes half a day...

## Project-Related Questions

<!-- > Pascal to JVM compiler
> 
> The aim is to design and implement a compiler for the classic programming language Pascal (or another language), using Java Virtual Machine code as the target language. If time permits, language extensions can be explored.
> 
> Ideally the student will have taken PL(H). This project is an opportunity to put the concepts and techniques of that course into practice, as well as gaining an in-depth knowledge of the Java Virtual Machine.
 -->

1. In ANLTR, I'm curious why there is no need to include things being handled to skip channel inside any parser rules.

* i.e. things like comments, EOF, whitespace
* ![](https://i.imgur.com/dQBCcue.png)


2. When implementing the custom visitor, is the using of CASE statements a common way to choose the desired alternative?

* i.e. are there any other ways to make alternative desicions? or should we always using `#` to markup each alternative

```java
void prog() {
    switch ( «current input token» ) {
        CASE ID : assign(); break;
        CASE IF : ifstat(); break;
        CASE WHILE : whilestat(); break;
        ...
        default : «raise no viable alternative exception»
    }
}
```  

3. Is that worth mentioning ANTLR4 features (supporting left recursive, `ALL(*)`) against other automation tools though the dissertation should focus on compiler itself

* i.e. first contrast bottom-up and top-down methods, then clarify why choose ANTLR as the top-down implementation tool against other tools

4. (**if have time, currently don't think these have higher priority than the extension direction of implementing other Pascal features**) Could '*encapsulate the implemented compiler*' be an extension of this project? (usage/deployment extension)

* i.e. develop an command line tool for usage, then deployed both on NPM and dockerhub
    * consider develop IDE plugin seems little bit tricky to handle, while there are various NodeJs tutorials on how to make command line tools.

5. (**if have time, same as above**) Apart from the CMD tool, I'm also thinking about utilising the AST generated from ANTLR

* like
    * generating the **AST visualisation** files (when user request in command line)
        * haven't found any existing API to utilise but seems generating the `.dot` files then visualise works
    * **static analysis** the source Pascal program (might be lots work to do, and a little bit off the topic)


# Blockers

--

# This week Plan (After Meeting)

* Orgnize minutes of this week
* Should finish looking Pascal syntax
    * quick looking website resouces
    * looking book to reinforce the understanding
* Would finish reading the book *The Definitive ANTLR 4 Reference* and ANTLR4 repo docs
    * make sure could utilise some features of ANTLR4( grammar modularity, semantic predicate etc.) for project extension and maintainity
* Continue looking in the suggested book (*Programming language processors in Java*)
* Adjust the ‘week-by-week plan’ according to the progress so far
    * make it more detailed, as courseworks already impeding the progress somehow
* Consider how to allocate the time finish reading


---

# Week 6 - Meeting Minutes

would be organized after meeting... 

## 4th Meeting: 25/10/21 - Mon

time: 12:00 - 12:30

## Things Agreed & Acknowledged

1. **Is that worth mentioning ANTLR4 features (supporting left recursive, `ALL(*)`) against other automation tools though the dissertation should focus on compiler itself**

* Just mention ANTLR is powerful. Enable us generating the compiler components automatically without other operations.
* Contrast to other old tools, when addressing the ambiguity problem, it may involve writing the rules for each alternative. While ANTLR could resolve the ambiguity problem by left recursive.

2. Experiment the existing Pascal grammar with exmaples from books
3. Focus the book of current stage rather than try to finish several looking once.

## Before Next Meeting

* Organize previous meeting minutes
* Experiment with the existing Pascal grammar, if does not work try to amend it.
    * generate the lexer & parser - contactic analysis
* Finish looking of book *The Definitive ANTLR 4 Reference*