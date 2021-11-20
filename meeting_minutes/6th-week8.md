# 6th Meeting: 08/11/21 - Mon

time: 12:00 - 12:30

# Things Agreed & Acknowledged

1. Start working on the contextual analysis of simple constructs

* objectives: get those basic constructs worked first, have the basis idea prepared for implementing the complex constrcuts and refinements

2. Choose the stacked-based symbol table which is more straightforward

* when comes to find a specific identifier, check the most recent stack frame(the toppest one), if cannot find the one declared, continue searching for the frame underneath. (If still cannot find, report the contextual errors)
* Should have one hashtable for the global scope, and a stack for all the local scopes? **Might exist other efficient structures but leave for now**

3. How should we relate the field mappings of a record? (check whether a specific field declared or not?)

* Might consider extend the fields of symbol table, enable us to connect record field with its memebers (another container/another scope)

4. Reserved words shuld be put directly in the predefine() method - enough for now

# Before Next Meeting

* Organize previous meeting minutes
* Should be okay to start working on the contextual analysis of some simple constructs
* Do more research about the contextual analysis stage
* Might continue looking in the suggested book (*Programming language processors in Java*)