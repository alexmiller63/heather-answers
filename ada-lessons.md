# Learning Ada Through a Real Project

ChannelDial could eventually become the seed of a teaching tool for learning Ada through real project evolution.

The lessons would not be contrived exercises. A learner could move through the commits and see why each concept appeared: first a program, then a record, then a concrete record instance, then an array of records, then iteration, then searching, validation, persistence, and so on.

The teaching pattern is simple:

**Each commit is one lesson. Each lesson leaves the program working. The project gradually becomes useful software.**

The source code itself can identify the lesson being demonstrated with comments such as:

```ada

--  Lesson 3: Build a collection of records using an Ada array.

