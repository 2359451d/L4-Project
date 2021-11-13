# 3rd Meeting: 18/10/21 - Mon

time: 12:00 - 12:30

# Things Agreed & Acknowledged

1. Consider modifying the structure of comment lexer rules

* do not put it inside the parser rules, best practice: handle to skip channel

2. Parser rule of String (QUOTE STRING QUOTE) might be changed to something like (`'`|STRING)

3. Reference the implemented Pascal grammar of ANTLR repo and the suggested book

4. How to process the built-in methods?

* no need to include all the built-in method identifier as the lexer rules, just left `ID()`， as assumed user-defined method would override the same identifier
    * need way to identify between them later on(searching order etc)

5. Reserved word should come first before any other lexer rules

* consider ANTLR features, to handle the ambiguity, would choosing the top first alternative (or choose the rule which match the longgest string as possible).

# Before Next Meeting

* Organize previous meeting minutes
* Should finish looking Pascal syntax
    * quick looking website resouces
    * looking book to reinforce the understanding
* continue looking in the suggested book (*Programming language processors in Java*)