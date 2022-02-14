# Plan

* Project Title: Pascal to JVM compiler
* Student Name: Yao Du
* Student ID: 2359451d
* Supervisor Name: Simon J Gay

Week-by-week plan for the whole project. Update this as you go along.

## Winter semester

* **Week 1**
* **Week 2**
* **Week 3**
* **Week 4-6**
  * looking in the books
    * *programming language processors in java* and
    * *introduction to Pascal*
  * research about other concepts if discovered along the way
* **Week 7-8** [got 1 solo AE remain: should take 3~4 days]
  * contextual analysis
  * **week 7** - might mainly focus on research things
    * if still got time, might do the implementation
  * **week 8** - implementation
    * if got time, move to the code generation
* **Week 9-10** [got 1 or 2 group AE remain: should take 3~4 days]
  * code generation for the basic constructs - hopefully
* **Week 11 [PROJECT WEEK]**
  * start working on status report
    * if still got things remain, continue work on the implementation
* **Week 12-13 [PROJECT WEEK]** Status report submitted.
  * Should almost finalise the status report before Friday 17:00 (end of week13 12/17?)
  * PSI exam - 12/09[09:00am]

## Winter break

* might finalise the compilation for complex constructs first if have not done
* extend the project if have time
  * focus on implementation of **other Pascal features** (OO feature etc.)
  * if got time, might research more about how to make a **command line tool(alternative: alias script)** for usage. Or move to other extension if better ideas found

## Spring Semester

* **Week 13/1**
* **Week 14/2**
* **Week 15/3**
* **Week 16/4 (31/01-06/02)**
  * Finish JVM-related reading
  * Split contextual analysis test suites into small unit (where each case only throws one error or no errors)
  * Experiment code generation with more components (starts from simple one first)
    * **Assumed challenges**: type definition, records, referenced-types(arrays, pointers), nested procedures/functions
* **Week 17/5 (07/02-13/02) - 18/6 (14/02-20/02)**
  * Continue code generation coding
* **Week 19/7 (21/02-27/02) - Week 20/8 (28/02-06/03)**
  * Continue code generation coding if not finished
  * Conduct evaluation, priority:
    * passed test number
    * compile time
    * execution time
    * memory leaks detection (need to figure out a way to gather heap tracking log when running pascal programs using existing compilers)
    * test coverage (result would somehow involve unrelated classes, so left with low priority)
* **Week 21/9 (07/03-13/03) - 22/10 (14/03-20/03)**
  * Write dissertation and polishing. Expectedly sent draft two weeks before the deadline
* **Week 23/11 (21/03-27/03)** Dissertation submission deadline and presentations.
  * **Deadline date**: 25/03
  * Write dissertation and polishing. Presentation video.