+++
title = "On Teaching Python"
date = "2025-05-20T17:48:12+01:00"
#dateFormat = "2006-01-02" # This value can be configured for per-post date formatting
author = ""
authorTwitter = "" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
draft = true
+++

## Introduction

A while back I was asked to teach Python classes at my school. After a few 
hours of research I drafted a plan on how to teach Python from the 
most basic fundamentals up to a point where the students were comfortable 
writing code to completed simple tasks. The classes ended up being scrapped 
but I thought it'd be interesting to put it up here in case I got another 
oppurtunity like that again or if someone else was interested. The curriculum itself 
isn't anything crazy but it was suitably different from how I was taught that I 
thought, so I hope somebody else out there finds it helpful. 

## Week 1 

I'd start with the REPL. Mostly because the REPL is severely underrated by most 
programmers I've spoken to. Being able to experiment with your code, find 
documentation, and such is invaluable for a beginner programmer and the REPL 
is a much better venue for that then text files. Furthermore, in other Python classes
I've been too, lots of people had trouble telling the difference between the IDLE 
in script mode and repl mode then once they were done with that they simply forgot 
about the REPL. 

>> REPL stands for (READ-EVAL-PRINT-LOOp), when you enter something into the REPL 
>> it **reads** it, then **eval**uates it then **prints** the result. That's why 
>> whenever you enter something into the REPL. For example 2 + 2. You get the result 
>> immediately on the next line. 

So we'll probably start out by just entering things into the REPL. Mathematical Expressions, 
numbers, strings- stuff like that to get them used to seeing the values. Make them do 
a few calculations with mathematical constants (pi and the like). Make them do these calculations
over and over again with the same constants. Use this to introduce how convenient being able to re-use 
values would be, if you define a value with a name and refer to it over and over again.  We'll 
use this to introduce variables 

>> Variables are like containers that we put values into so we can refer to them later. We call 
>> them variables because we can always change the value stored in a variable. 
>> Variables evaluate to the value that they hold

After they have a good grasp of what variables are we move on to functions. I think moving 
from variables to functions is somewhat simple conceptually since we're moving from 
naming values to naming computations. We use a similar method as earlier, we give them 
a bunch of exercises performing repetitive operations, probably with strings as they are more
interesting, then show them how to use functions to factor out similarities. It's important 
to emphasize that functions only evaluate to what they return. Also differentiate between 
expressions and statements. Once they are accustomed to writing and using functions, feel 
free to introduce to useful built-in functions. Particularly print(), make sure to differentiate
between Print's return type and what it does. 


>> Blah, Blah, Blah about functions. 


At this point, writing functions into the REPL will probably be somewhat extremely cumbersome
especially when errors occur. We can move on from here to writing in python files, emphasize
that most programming is using files rather than repl. The `print` function will be really 
handy for this. Start with plain text files using notepad or some other barebones text editor. 
then run it from the command-line. This is to make sure students understand that there's no 
magic behind running code with and IDE. After they write a few simple programs like this: 
Hello World, FahrenhaitToCelcius, so on and so forth we'll move them to an actual code editor
probably Thonny or IDLE. I'd love to encourage them decide on a code editor themselves.

Even with the very little we've covered this chapter. With a bit of imagination we 
can write some really simple yet interesting programs. Using input() we can write 
function that takes input from the user and performs simple operations on them. Nothing 
crazy perhaps but hopefully enough to get them interested in writing code themselves. 

If we're willing to introduce using libraries a bit early we can use the Turtle module to 
write simple gui's that would definitely grab people's interests. Or using the request library
we can get data from REST apis. There are tons of apis out there that would definitely 
get people interested and consuming there is fairly easy so we can get them writing 
scripts that **do** something fairly early even without conditionals or looping. The point 
is to get them on something that would make them more eager to write code on their own. 
 
