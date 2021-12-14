---
title: Week 13 Meeting Report
tags: Templates, Report
description: Weekly Meeting Report
---

# Week 13 - Meeting Report

Time: 13/12/2021 Mon 12:00-12:30

# Week 12 - Recap

* Things about the status report
    * possible motivations, aims, problems and risks

# Week 12 - Progress

* Fixed driver bug where the number of **token recognition errors** raised base `Lexer` class won't be recorded.
    * ![](https://i.imgur.com/5ZszKcj.png)
    * Though errors are reported for invalid token, but the number of syntax errors won't increment
    * Doesn't work in the driver of both syntactic & contexual analysis
    * **Works now, where the errors are processed seperately and printed into two lines**
        * ![](https://i.imgur.com/gJqvS4Y.png)
        * ![](https://i.imgur.com/oTfS20l.png)
* Setup example unit test case for the syntactic analysis driver `PascalParse`

# Questions

## Project-Related Questions

1. The evaluation part of the project was mentioned in our L4-Project Dissertation guidance online live session, and it mentioned that **run experiments to gather evidence** and figure out what could be the **dependent variables and independent variables**

* I'm not sure what kind of things could be evaluated  of the project...
    * compiler performance (compling time)
    * test suites coverage
    * ...
* ![](https://i.imgur.com/9p2GRp3.png)
* ![](https://i.imgur.com/90PiKRA.png)

2. If there is a need to introduce automatic testing for the compiler, is that enough to cover: 

* **regression test**
    * cheap and easy way: every time you fix a bug in your compiler, put a suitable test into your regression suites
    * I suppose this is what I've done so far **manually**, debug and cover a instance when discovered
        * ![](https://i.imgur.com/4xhzitA.png)
* **run existing test suites if found more**
    * seems there exists some Standard Pascal(ISO 7185) test suites, but not sure whether all of them are approachable or not
    * one example - **Pascal Acceptance test** (PAT) & **Pascal Rejection Test** (PRT)
        *  *a series of tests in one file that go through each feature of ISO 7185 Pascal. If a ISO 7185 Pascal implementation can compile and run this correctly, then it is substantially compliant with ISO 7185 Pascal.*
        *  The PAT test should compile and run correctly, and is a “positive” indication that the implementation compiles standard structures and gives standard results. The PRT is the opposite.
        *  ![](https://i.imgur.com/77RcZ0h.png)
        *  ![](https://i.imgur.com/LkPTo54.png)


# This week Plan (After Meeting)

* Orgnize minutes of this week
* Continue working on the contextual analysis
* Finalise Status Report 
    * send the PDF via email by Friday (17th December @ 5PM)

---

# Week 13 - Meeting Minutes

would be organized after meeting... 

<!-- ## 7th Meeting: 15/11/21 - Mon

time: 12:00 - 12:30 -->

<!-- ## Things Agreed & Acknowledged -->

<!-- 1. Start working on the contextual analysis of simple constructs

* objectives: get those basic constructs worked first, have the basis idea prepared for implementing the complex constrcuts and refinements

2. Choose the stacked-based symbol table which is more straightforward

* when comes to find a specific identifier, check the most recent stack frame(the toppest one), if cannot find the one declared, continue searching for the frame underneath. (If still cannot find, report the contextual errors)
* Should have one hashtable for the global scope, and a stack for all the local scopes? **Might exist other efficient structures but leave for now**

3. How should we relate the field mappings of a record? (check whether a specific field declared or not?) 

* Might consider extend the fields of symbol table, enable us to connect record field with its memebers (another container/another scope) -->

<!-- ## Before Next Meeting

* Organize previous meeting minutes -->
<!-- * Should be okay to start working on the contextual analysis of some simple constructs
* Do more research about the contextual analysis stage 
* Might continue looking in the suggested book (*Programming language processors in Java*) -->