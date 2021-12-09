
## *[title]* 
#### *Yao Du* 
#### *2359451d* 

## Proposal
### Motivation
*[Clearly motivate the purpose of your project; why someone would care about what you are doing]*

### Aims
*[Clearly state what the project is intended to do. This should be something which is measurable; it should be possible to tell if you succeeded]*

## Progress
*[Briefly state your progress so far, as a bulleted list]*

* Syntatic Analysis implemented using automatic generating tool: ANTLR(4.9.1). Both runtime lib, docker image, scripts are ready for regenerating lexer & parser if any.
* Partial contexual analysis implemented
  * data types
    * simple types: integer, real, char, boolean
  * declarations
    * variable declarations
    * procedure declarations
  * statements
    * assignment statements
    * repetitive statments
      * while
      * for
      * repeat...until
    * if statments

## Problems and risks
### Problems
*[What problems have you had so far, that have held up the project?]*

* Need to design a suitable/workable Type descriptor class for those built-in Function/Procedure. Currently these related implemention are left and broken.
* There exists several boilerplate code of the `PascalCheckerVisitor` (contexual analysis program).
* Entire project is badly documented/commented.
* Currently several contexual analysis things unimplemented:
  * Data declarartions
    * const, type
  * Data types
    * enumerative, subrange
  * Other constructs
    * arrays, records, sets, files, pointers
  * Statement
    * procedure, function
    * Case
    * GOTO
  * Varaible declaration
    * function
  * operators
    * in
    * relational operator (`=`,`<>`,`<`,`>`,`<=`,`>=`) only implemented for primitives & string
  * Nested Proc/Func Declaration
  * Builtin Proc/Func

### Risks
*[What problems do you foresee in the future and how will you mitigate them?]*

* If these built-in procedures/functions are included in source programs, it would throw contexual analysis error. **Mitigation:** it is workable if figure out a possible pattern to describe them. Also, it is worth amending the grammar to describe the parameter list for every builtin symbol.
* Though it seems workable to define those built-in procedures/functions of standard Pascal(ISO 7185). The extension of Pascal would involve a number of built-in components e.g. those of Free Pascal. **Mitigation:** regardless of the dialect choosen, should figure out a uniform way to introduce these components if possible. Currently it seems hard to implement by searching through the runtime library (at least true for Free Pascal).
* Some definition of specific constructs are vague. Some concepts may not mentioned explicity in standard Pascal convention (ISO 7185). Online resources are confusing where it does not mention whether specific behavior is standard or not. **Mitigation:** would mainly focus on ISO 7185, avoiding introducing subject understanding.
* Some rules of current grammar might not be metioned in standard convention e.g. `CASE-OF-ELSE` statement. Unclear whether current grammar need modify. **Mitigation**: since would focus on standard Pascal, if these are truly not standard would not implement them for now. If causing problems, would amend the grammar.

## Plan
*[Time plan, in roughly weekly to monthly blocks, up until submission week]*

## Winter semester

* **Week 1-3**: Setup github repo and meeting pattern & Work on Syntactic Analysis
  * **Deliverable**: TBC
* **Week 4-6**
  * looking in the books
    * *programming language processors in java* and
    * *introduction to Pascal*
  * research about other concepts if discovered along the way
  * **Deliverable**: TBC
* **Week 7-8**
  * contextual analysis
  * **week 7** - might mainly focus on research things
    * if still got time, might do the implementation
  * **week 8** - implementation
    * if got time, move to the code generation
  * **Deliverable**: TBC
* **Week 9-10**
  * continue contextual analysis, objectives: implements the simple constructs first
    * Type Descriptor Design (primitives, array, records, etc.)
    * Then move to the custom visitor implementation (simple constructs first)
    * Contexual Analysis Driver
  * **Deliverable**: TBC
* **Week 11 [PROJECT WEEK]**
  * would start working on status report
    * if still got things remain (contextual analysis), continue work on the implementation
  * if still got time, would start research **code generation & JVM & class files** (would focus on research first, but not very confident about the code generation implementation)
  * **Deliverable**: TBC
* **Week 12-13 [PROJECT WEEK]**: Status report submitted.
  * Try to finalise **Contexual Analysis**
  * Would have full time work on project in week 13, so if able to finish the contexual analysis of the remaining constructs, would start researching about **code generation**
  * Should almost finalise the **status report** before Friday 17:00 (end of week13 12/17?)
  * **Deliverable**: TBC

### Winter break

<!-- * research more about Pascal compiler (detailed symbol table structure design)
    * But before this, should consider what kind of information from contexutal analysis are really needed to be provided in code generation. (Do not design a symbol table by intuition which doesn't help at all) -->

* might finalise the contexual analysis for complex constructs first if have not done
* Start working on code generation implmentation and researching
  * JVM things (mainly class file)
  * possible books for reference:
    * JVM Specification (JDK8)
    * Understanding the JVM Advanced Features and Best Practies, Third Edition
* Extend the project if code generation finished
  * focus on implementation of **other Pascal features** (OO feature etc.)
    * Should really consider which Pascal dialect to choose (**better a well-documented one, otherwise would definely cause confusion**).
  * might would like to research about the **intermediate code optimisation**
  * if got time, might research more about how to make a **command line tool** for usage. Or move to other extension if better ideas found