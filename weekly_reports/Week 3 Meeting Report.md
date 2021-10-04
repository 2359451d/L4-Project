---
title: Week 3 Meeting Report
tags: Templates, Talk
description: View the slide with "Slide Mode".
---

# Week 3 - Meeting Report

Time: 04/10/2021 Mon 12:00-12:30

# Who am I?

- Yao Du

# Week 2 - Recap

--

# Week 2 - Progress

* done half revision of the PL course
    * Lecture 1-8 done, 9-15 remain
* github repositoires setup (Github Id: 2359451d)
    * dissertation
    * source code
    * progress recording (docs like meeting minutes, meeting report, timelog)

# Questions

## General Questions

1. How should I address you?

2. Is that alright we just keep this form of weekly meeting for now? Or shall I send you emails to confirm the meeting arrangements before the meeting just in case you are busy and the arrangements might be changed?

3. Is that alright that I show my weekly report in this way
    * bring the printed documents to the in-person meeting
    * show the slides or markdown file if we have a remote meeting

4. If we have a remote meeting, may I record our meeting for the minutes as I might kind of lose track of some words.

5. Is that alright I public all the level 4 project repositoreis in Github?

6. Currently I've set up 3 repos for the project (with soft links to quick access each other). Is this ok or would you suggest integrate everything in one repository. 
    * ![](https://i.imgur.com/Tvq2I5o.png)

7. I'm curious about when would majority of students start working on the dissertation draft?
    * Was that after all the source code finalised i.e. Semester 2...

8. When would be the best time to send you the draft before the deadline?
    * like 2 weeks ahead or ... 

9. Is there any other things that should be awared of?
    * like how much the compiler should be completed this semester, considering the workload of coursework would accumulate later on 


## Project-Related Questions

> Pascal to JVM compiler
> 
> The aim is to design and implement a compiler for the classic programming language Pascal (or another language), using Java Virtual Machine code as the target language. If time permits, language extensions can be explored.
> 
> Ideally the student will have taken PL(H). This project is an opportunity to put the concepts and techniques of that course into practice, as well as gaining an in-depth knowledge of the Java Virtual Machine.

1. How much extent should I know the Pascal？
    * ![](https://i.imgur.com/s0PQlII.png)

2. How much extent should I know about the JVM
    * JVM memory structures, gc techniques, optimisation...

3. How much extent should I know the java bytecode and the bytecode(.class) file?
    * ![](https://i.imgur.com/idcD7VY.png)
    * ![](https://i.imgur.com/hf3oE6X.png)

4. Should the Pascal to JVM compiler being written in Java?
    * Similar to what we have done in PL coursework...

5. It said that there is two ways to converts a token stream into an AST: Top-Down(Recursive descent parsing) & Bottom-up methods, should all of them being implemented and covered in the dissertation?

6. Shall I use the automation tool to generate the compiler components or implement them manually?
    * And if allowed, should I try other tool(lex yacc, javacc) or ANTLR is enough

7. Shall I implement the tree walkers in both Visitor pattern and Listener pattern and mentioned in dissertation?

8. Would the dissertation focus on how the compiler implemented in each stage or something else as it is a research style project

9. what would be the most challenging part of this project?
    * I recall in PL coursework it took some thinking when processing the address in code generation stage... 

# Blockers

--

# This week Plan (After Meeting)

* Orgnize minutes of this week
* finish revising the PL lecture
* take a look in suggested book (*Programming language processors in Java*)

---

# Week 3 - Meeting Minutes

would be organized after meeting...

* [see here](https://github.com/2359451d/L4-Project-Record-Repo/blob/master/meeting_minutes/1st-week3.md)

also below

## 1st Meeting: 04/10/21 - Mon

time: 12:00 - 12:30

## Things Agreed & Acknowledged

* if got time, try to **extend the project**
  * start from the direction of extended Pascal feature
  * ![](/static/2021-10-04-21-32-24.png)
  * or other possibility - integrates this compiler into IDE (plugin component? - anyway might be lots work to do)
* in semester 2, would mainly focus on the dissertation writing
* **when would be the best time to send the draft**?
  * ensure enough time being left, and sent before the deadline as time goes
  * then got enough time to revise and discuss further
* **should plan myself the project things as time goes**
  * progress each week
  * progress each semester
  * balance the workload, and assess the progress difference between weeks, (to see whether certain week left too much things to do...)
* **How much extent should know Pascal**
  * just like other PL, basic constructs
  * NOTE: the pointer types might be tricky to deal with, cause' the pointer types of Pascal not similar to what we have in C. (implemented more bottom-level as Java?)
* **How much extent should I know about the JVM/bytecode/class file**
  * target - able to emit JVM bytecode, and study the concepts along the way
* **two ways to convert a token stream into an AST: Top-down(ANTLR) & Bottom-up methods, which one to choose and should all of them being metioned in dissertation?**
  * dissertation things left here for now. But ANTLR use the top-down method, might be straightforward
* **ANTLR is powerful compared to other automation tool, so can just choose ANTLR**
* **the tree walkers could be implemented in Visitor pattern(more straightforward)**
  * but can have a look of Listener pattern if interested
* **Things would be coverd in dissertation now left, would be mainly disscussed later on**
* most challenging part
  * it depends
* **should this compiler being written in JAVA**
  * depends but I'm familar with JAVA
  * NOTE: consider the bootstraping compiler...might first have a compiler "Pascal to JVM" written in JAVA, then reversely have a compiler "Pascal to JVM" written in Pascal for bootstraping...
    * might be tricky...

## Before Next Meeting

* Organize previous meeting minutes
* finished revising the PL course
* take a loo in suggested book(*Programming language processors in java*)
* have a general plan for each week (an overview)
  * then for each week could find the right direction to follow and focus