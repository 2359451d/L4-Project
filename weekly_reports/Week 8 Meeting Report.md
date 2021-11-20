---
title: Week 8 Meeting Report
tags: Templates, Report
description: Weekly Meeting Report
---

# Week 8 - Meeting Report

Time: 08/11/2021 Mon 12:00-12:30
<!-- http://silcnitc.github.io/data_structures/global-symbol-table.html -->

# Week 7 - Recap

previous week we went through:

* Should be okay not to change the implemented Pascal grammar found
* Should research about the JVM through next several weeks

# Week 7 - Progress

* Finished reading the book *The Definitive ANTLR 4 Reference*
* Research about contextual analysis

# Questions


## Project-Related Questions

<!-- > Pascal to JVM compiler
> 
> The aim is to design and implement a compiler for the classic programming language Pascal (or another language), using Java Virtual Machine code as the target language. If time permits, language extensions can be explored.
> 
> Ideally the student will have taken PL(H). This project is an opportunity to put the concepts and techniques of that course into practice, as well as gaining an in-depth knowledge of the Java Virtual Machine.
 -->
 
1. While conducting the type checking process, does the order of every nodes being checked matter?

* Or just always follow postorder-style checking (left->right->root)

2. In current stage, is that enough just put all the reserved words into the symbol table inside the predefine() method?

3. What would be the best practice to handle the symbol tables of nested scopes?

* like when there are nested function calls, I'm currently assuming create independent symbol tables for each scopes except for the global scope. Then each scope has its own mappings. But seems would take up much space.

```pascal
program fibonacci;

function fib(n:integer): integer;
begin
    if (n <= 2) then
        fib := 1
    else
        fib := fib(n-1) + fib(n-2); (* nested recursive call *)
end;

var
    i:integer;

begin
    for i := 1 to 16 do
        write(fib(i), ', ');
    writeln('...');
end.
```

![](https://i.imgur.com/SvXHDPQ.png)
![](https://i.imgur.com/Qmgl2Xc.png)

4. How should we relate the field mappings of a record? (check whether a specific field declared or not?) 

* Assuming when there exists global/local variable with the same field name?
* I'd assume it won't work if just simply inserting the field mapping(identifier-type) into the symbol table...
* Shall we use linked list to implement? Or just connect the record type with a new container which contains all the field mappings?

```pascal
type date = record
    month:1..12;
    day:1..31;
    year:1900..2000
    end;
var
    month: integer; (* global variable, not a field of record date*)
    day:date;
```

# Blockers

--

# This week Plan (After Meeting)

* Orgnize minutes of this week
* Should be okay to start working on the contextual analysis of some simple constructs
* Do more research about the contextual analysis stage 
* Might continue looking in the suggested book (*Programming language processors in Java*)

---

# Week 8 - Meeting Minutes

would be organized after meeting...

## 6th Meeting: 08/11/21 - Mon

time: 12:00 - 12:30

## Things Agreed & Acknowledged

1. Start working on the contextual analysis of simple constructs

* objectives: get those basic constructs worked first, have the basis idea prepared for implementing the complex constrcuts and refinements

2. Choose the stacked-based symbol table which is more straightforward

* when comes to find a specific identifier, check the most recent stack frame(the toppest one), if cannot find the one declared, continue searching for the frame underneath. (If still cannot find, report the contextual errors)
* Should have one hashtable for the global scope, and a stack for all the local scopes? **Might exist other efficient structures but leave for now**

3. How should we relate the field mappings of a record? (check whether a specific field declared or not?)

* Might consider extend the fields of symbol table, enable us to connect record field with its memebers (another container/another scope)

4. Reserved words shuld be put directly in the predefine() method - enough for now

## Before Next Meeting

* Organize previous meeting minutes
* Should be okay to start working on the contextual analysis of some simple constructs
* Do more research about the contextual analysis stage
* Might continue looking in the suggested book (*Programming language processors in Java*)