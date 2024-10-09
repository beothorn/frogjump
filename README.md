# frogjump
An experiment with AI

# The idea

Context is everything. 
But, it is spread through lots of places. Documentation, tasks, change history.  
The context is also big, too big too be all at once inside one head.  
If one needs to fullfill a requirement, it would be unresonable to try doing it without evaluating the context (documents, requirements) first.  
But, we do it with the LLMs. 
If a system is built from ground up to include documentation and comments, if tasks and documentation live inside the same repository, if the LLM is given a small set of commands that exposes just tiny bits of the system what would happen?

Below some notes.
.......

Documentation pass
Single paragraph explanation

Class level 
List public functions

Package level 
Child packages 
This package

Module level
Business explanation 
Architecture 
Package overview

Tests
Scenario description

Root package 
Business reasons

----
Regenerate docs pass 
Code generation with tests and docs


Code gen
- docs
- public functions from related classes 

Needs 
Class outline generation 


Code, docs and tasks should be self contained  

No jira, no wiki all lives on the same codebase  
Bugs are on a folder bugs  
Tasks on a folder tasks  
A pass needs to implement those and delete/move the entries to done or mark as done  
Each interaction solves tasks and update docs
The AI needs to be able to query the code 
So, call hierarchy, get implementors, do text search, go to function implementation 

Can we look at only the function and the class fields?    
Documentation needs to be query? Comments?   


Commands  

getOpenTaks
markTaskAsDone
listFiles [folder]
explainClass [qualified name] # Prints class javadoc
describeClass [qualified name] # Prints public functions with java doc first sentence
printFunction [function reference] # Prints function with java doc, referenced imports and referenced fields
deleteFunction 
addField
removeField
createClass
deleteClass
build
printPackageDoc
createPackage
createPackageDoc
???? 


```
"On two occasions I have been asked [by members of Parliament], 'Pray, Mr. Babbage, if you put into the machine wrong figures, will the right answers come out?' I am not able rightly to apprehend the kind of confusion of ideas that could provoke such a question."
-- Charles Babbage
```
