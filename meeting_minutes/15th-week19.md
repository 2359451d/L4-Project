# Week 19/7 - Meeting Minutes

would be organized after meeting... 

## 15th Meeting: 11/10/22 - Tue

time: 14:00 - 14:30

## Things Mentioned

* should switch to writing, so we have things to discuss related to the report
    * might want to implement constructs that havent done if have time (but **low priority** for now)
* Design part
    * Consider write about the standard compiler architure (3 stages)
        * what kind of things might need to do in each stages
        * like
            * syntactic
                * lexer, generate token based on production rules
                * take token, generate AST
            * semantic
                * consume AST (visitor pattern),
                * type check
                * scope check
            * code generation
                * code selection
                * emit target code (bytecode)?
        * substitude concrete concepts into standard compiler design?
* Implementation part
    * Seperate into 3 stages (Main sections)
        * language constructs as subsections in each stage?
            * expression
            * proc,func
            * control flow
            * ...
* Future Work
    * Might cover features that not implemented, and ideas about how these might be implemented
        * e.g. nested proc,func decl, pass them as parameter. 
* Reason of why only basic features of std Pascal implemented => more complex features are built upon simple one
    * if start from complex one, might need extra refactor work to do as time goes. As complex features might depends on different basic constructs, and it is hard to determine the uniform behavior of if starts from complex one.
    * go back might find that, other features worked entirely different, unexpected
    * **though only basic subset of Pascal features implemented, still the program can be expressed in straight forward way**