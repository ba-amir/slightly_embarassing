+++
title = "Why Perl"
date = "2025-05-18T22:15:34+01:00"
#dateFormat = "2006-01-02" # This value can be configured for per-post date formatting
author = ""
authorTwitter = "" #do not include @
cover = ""
tags = ["Perl", "Programming Languages"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
draft = true
+++

## Introduction

Perl is a filthy little gremling of a language, and that's exactly why I love it so much. 
Perl doesn't care about conforming or being elegant. No, Perl 
relishes in being clever, dastardly and much more fun to write in than any other language out there. 
It's no wonder that Perl's motto is 
There is More Than One Way To DO It. No matter what you're doing or why you're doing 
it Perl will always give you options. Some good, some bad but Perl always allows you, 
the programmer, to pick your poison. 

Perl's no holds-barred approach to programming makes it an incredibly 
useful tool to whip out at a moment's notice and get dirty with whatever 
is in front of you. Which makes it immensely suitable for scripting. 
That said, Perl isn't a magic bullet, like all programming languages Perl 
has its own trade-offs and guarantees. Personally, I wouldn't recommend 
Perl for a large team of programmers where some first have to be trained
in the language. But when it comes to having fun while writing code.
Perl is always going to be at the top of my list.

Now of course, most of the current audience is going to want more than 
a few powdered words before deciding to take a new tool for a spin. 
That's why I've created this article to outline six of what I consider
to be six of Perl's most interesting, unique and powerful features. Of course, 
this list is entirely subjective and will probably be completely different 
for someone more experienced with the language. These are the features that 
most excited me and I hope to share some of that excitement with you guys. 

Before we continue, some of the topics we will discuss subsequently 
will be shocking, bizarre, possibly nauseating and probably not fit 
for discussion among civilized company. If you are faint of heart 
or unsound of mind, continue at your own peri. (I'm so sorry, I couldn't resist).

## 1. Sigils!!! 
    
```Perl
my $name = "foo"; 
say $name;
```

When you look at the above snippet of Perl code, your first question is likely to be 
"what's with the dollar signs?" as opposed to "what kind of name is foo?".
Those are called sigils, they are used to indicate the data type of a variable. 
There are are three main sigis to consider, each corresponding to one of Perl's builtin dataypes. 
Yes, Perl has only three data types and none of them is int. They are: 

1. Scalars ($name)
2. Arrays of Scalars (@name)
3. Associative Hashes of Scalars (%name)

You probably recognize all three from other programming languages. Scalars are single-value objects; 
Arrays correspond to Python Lists and Associative Hashes are Dictionaries or Maps. Something I really love  about sigils 
is that they allow you to have a separate namespace for each data type. Now you can live out your darkest
fantasies of naming both a single number and a list of numbers the same thing. 

```perl 
sub max(@num) {
    my $max = shift @num; # shift removes and returns the first element of an array
    for my $num (@num) {
        if ($num > $max) {
            $max = $num;
        }

    }
   return $max 
}

```

In the foreach loop above we can use num to refer to both the current number being considered and the array of numbers
passed in as an argument. Without sigils, you'd have to come up with two different names when one would suffice. It's 
an extremely common occurence when programming to have a thing and a list of that type of thing. In Haskell, there's 
a convention for that, x for thing and xs for thing's list. In other programming languages I use x and x_list, Perl 
completely sidesteps this problem using sigils. A small win, a win regardless.

I imagine that sigils may simplify some of the compiler's work since by looking at a variable it already knows what
type it is.

Where sigils will really start to shine though is when we start talking about context and why in Perl context matters.

## 2. Context Matters

As humans, we are no strangers to context. The statement "I need a kid's stool" means 
entirely different things depending on the context it's spoken. The same holds true for variables in Perl.

In Perl, Context refers to how an expression is used, that is, which operations 
```perl 
sub avg(@num)
    return (sum(@num)) / @num
}
```

This doesn't mean that an array will always return it's length when treated like a scalar. This behaviour 
depends entirely one the specific operator. Some operators simply return the last element of the list. This 
might all sound like a breeding bed for disaster but in practice it works surprising well. The Perl built-in 
funtions pay atttention to what the function is supposed to be doing. And the use context allow you to 
write more succinct code than would be otherwise possible. Sometimes at the cost of readability, Perl gives you 
the tools and expects you to do as fits your needs. But when writing your own functions, try to keep in mind
that your functions may not always be used how you initially intended so try and have reasonable defaults for 
scalars.



## 3. Regex Everwhere

Perl's Regular Expressions are so powerful that they've been shamelessly cribbed by programming languages
the world over. But none of these languages can copy what exactly makes Regex so terrifyingly effective. 


For one thing, Perl doesn't require you to lookup arcane documentation or trudge through miles of class 
constructors (cough, c++, cough), all you need is to write your regex like so `/<insert regex>/` and 
that's it. Not only is this all that is required to make a regex, it's also all you need to use one. 

You just need to slap that bad boy in an if statement and it automatically matches whatever's in Perl' 
default variable `$_`. If you would rather match your regex against another string the `=~` is also 
free for you to use. 

Don't forget that Perl is kind enough to perform your type conversions for you when you use string operators 
on numbers meaning that you can just as well apply a regular expression with a number with zero overhead. 
Which could be useful for stripping specific digits off a number, or transposing digits, or reversing digits 
the possibilities are endless.

## 4. Quote-like  Operators

In the previous heading, I showed you how to match your regex against other strings. But with Perl's regexes 
you can do so much more. Using Quote-like Operators you can for example: substitute strings that match 
regular expressions just like in your favourite text editor. 

## 5. Statement Modifiers

When writing really simple if statements with only one line or so, it can be a bit tedious having to write 
out the whole syntax in full just for a single line. Which might sound like a lazy complaint. The good 
thing is that Perl _wants_ you to be lazy. Which is where statement modifiers come in. 


```
die if condition
```

They also have the added advantage of reading more like natural English.
    - unless 
    - if 
    - until
## 6. Blocks and Higher Order Functions

Whenever I'm learning a new language, one of the first things I find our is whether they have Higher Order Functions. That is, 
functions that take other functions as input. Higer Order Functions are insanely useful for abstracting common patterns out 
of your code, especially things that you would have solved using yet another for loop. 


Perl also has anonymous functions or lambdas in the form of blocks. Which makes it super convenient for writing Higher Order Functions 
without being forced to rely on functions fully written out somewhere else.
