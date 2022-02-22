# Description

repo for docs & recording progress on level 4 project (**Pascal to JVM Compiler**), files contain:

* `timelog.md`
  * daily(at least) updated progress record

<!-- # Progress

## Basic Progress (**frontend of compiler**)

* syntactic analysis(might refine if needed): ![syntactic_analysis](https://progress-bar.dev/100/?title=done)
* contextual analysis: ![contextual_analysis](https://progress-bar.dev/28/?title=WIP)
* code generation (IR): ![code_generation](https://progress-bar.dev/0/)
* status report
* dissertation

## Project Extension Progress

* **OO Pascal feature or other dialects** (highest priority)
* **code(IR) optimisation** (optimizer, second priority)
* command tool
* docker & npm deployment
* other possible extension?
  * AST visualisation
  * etc.

## Reading Progress

* Introduction to Pascal, Second Edition: ![reading](https://progress-bar.dev/100/?title=done)
* Programming Language Processors in Java: ![reading](https://progress-bar.dev/10/)
* The Definitive ANTLR 4 Reference: ![reading](https://progress-bar.dev/100/?title=done)
* JVM Specification (JDK8): ![reading](https://progress-bar.dev/0/)
* Understanding the JVM Advanced Features and Best Practies, Third Edition: ![reading](https://progress-bar.dev/0/)

---

* **Other Books** that might help (might not have enough time to go through, in order of priority)
  * [Language Implementation Patterns](http://index-of.es/Programming/Pragmatic%20Programmers/Language%20Implementation%20Patterns.pdf)
    * 【Practical Examples】Build your own compiler/interpreter/translater, **same author of The Definitive ANTLR 4 Reference**
    * 31 genral design patterns
  * [Compilers: Principles, Techniques, and Tools](https://suif.stanford.edu/dragonbook/)
    * dragon book
    * http://www1.cs.columbia.edu/~sedwards/classes/2006/w4115-fall/dragonbook-language.pdf
  * [Engineering a Compiler, 2nd Edition](http://www.r-5.org/files/books/computers/compilers/writing/Keith_Cooper_Linda_Torczon-Engineering_a_Compiler-EN.pdf)
    * comprehensive concepts of how compiler is constructed. Emphasize on **code optimisation & code generation**
  * [Modern Compiler Implementation in Java](https://www.cs.princeton.edu/~appel/modern/java/)
    * tiger book (javaCC for frontend)
    * related-project
      * [java-like language(class, member func), frontend written in ANTLR4. Optimisation covered](https://github.com/merrymercy/compiler2017) (refer: ふつうのコンパイラをつくろう)
  * [ふつうのコンパイラをつくろう](https://github.com/aisuhua/Books-2/blob/master/%E8%87%AA%E5%88%B6%E7%BC%96%E8%AF%91%E5%99%A8%20%2C%E9%9D%92%E6%9C%A8%E5%B3%B0%E9%83%8E%E8%91%97%20%2CP445.pdf)
    * simplification version of the tiger book
    * how to implement cb(subset of C) compiler in java (generator: **javaCC**), [source code here](https://github.com/aamine/cbc)
    * also covers assembler, **linker**, Run-time env of Linux -->

# Weekly Meeting Report & Minutes

Report files would be saved on both **hackmd** and **github** (in `weekly_reports` & `meeting_minutes`)

weekly meeting report might cover the following sections:

* previous week recap (if applicable)
* progress of this week
* questions if any
* blockers if any
* plan for next week
* also meeting minutes for this week

## Quick Access to Weekly Reports in hackmd

* [week 3 - 1st meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/ryDzzuxEF)
* [week 4 - 2nd meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/SkEtOv04t)
* [week 5 - 3rd meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/By7piddBF)
* [week 6 - 4th meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/ByvdoGX8Y)
* [week 7 - 5th meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/H1Hyk8pUF)
* [week 8 - 6th meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/HJG1Hu8wK)
* [week 9 - 7th meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/r1uP6U6PF)
* 10-11 TBC
* [week 13 - 11th meeting](https://hackmd.io/@ztSWeeCGQVajqeMX2KsIXw/HJ9noc4ct)
* [week 15/3 - 12th meeting](https://hackmd.io/y9H6X6HjT0agqa4dkxR-tQ)
* [week 19/7 - 15th meeting](https://hackmd.io/fuxn_hNISy-8cFrdByKp2g?view)

quick access to related level 4 project repos (**only setup for this repo as it is hard to coordinate while the automation submodule updating script not working**, soft links might be removed if too cumbersome)

* dissertation
* source code

## Automation Updating Script

see file `submodule_script.bash`