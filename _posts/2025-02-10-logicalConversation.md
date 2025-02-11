---
layout: post #Do not change.
title:  "Having a logical concersation (literally)"
date:   2025-02-10 10:05:42 +0200
---
Some notes on *boolean algebra* and our language. <!--more-->


When "usual" people say "logical", they usually use it as synonym for intelligent, smart or simply right. But for a math geek, computer scientist, electrical engineer or something similar (maybe even philosophy students), logic has a second meaning.

That second meaning being *boolean algebra or digital logic or simply the mathematic field of logic*{% sidenote '1' "The difference between those things is basically non-existent. It's the same thing, but represented by different symbols."%}, a way of representing statements and drawing conclusions that is entirely guided by mathematics.

This type of logic is unseperably intertwined with our modern language, altough it is sometimes somewhat confusing. To see what I mean, let us just jump straight into it...

## 1. AND operators

Boolean Algebra like regular algebra deals with operators some more wieldy used (think plus or multiply) and some more uncommon (think mod and root). Today  we'll only discuss the most basic of those boolean operators.

Those operators take one or more statements, i.e. something that is either true or false (think correct or incorrect), and performs... well... an operation on them, i.e. returning a singular True or False statement. Digitial Logic takes this method and changes the statement for wires / signals that are either powered on or off. 

One of the most simple boolean operators is AND and I assume you see now, what I meant by *unseperably intertwined with our modern language*?

An AND operator takes two statements and returns *True*, if both statements are *True*, otherwise it will give *False*.

```
False AND False = False
True  AND False = False
False AND True  = False
True  AND True  = True
```

This of course translates well to language, where given that is a cloudless sunny day. The following statements can be said to be correct or incorrect.

It is cloudy and the sun doesn't shine. (Incorrect)
It is cloudless and the sun doesn't shine. (Incorrect)
It is cloudy and the sun shines. (Incorrect)
It is cloudless and the sun shines. (Correct)


## 2. The troubles with "or"

The OR operator also does what you'd expect. Given two statements of which at least one is true, the OR operator will return true. This gives the following truth table.

```
False OR False = False
True  OR False = True
False OR True  = True
True  OR True  = True
```

On the aforementioned cloudless sunny day, the following statemnets can be said to be either correct or incorrect.

It is cloudy or the sun doesn't shine. (Incorrect)
It is cloudless or the sun doesn't shine. (Correct)
It is cloudy or the sun shines. (Correct)
It is cloudless or the sun shines. (Correct)


The trouble with OR arises, when we have a question like "Is Jake a dog or a human?",

Here it is, where language tricks us. If we follow through on the meaning of the OR operator, this would mean that there are 4 scenarios:

1. Jake could be neither human nor dog.
2. Jake could be a dog, but not a human.
3. Jake could be a human, but not a dog.
4. Jake could be both human and dog.

The 4th statement, however, is reasonably bullocks. Here the "or" implicity meant an XOR instead of an OR operator. A XOR - short for exclusive-OR - operator returns true, if exclusively one of the input statements is true. A XOR can explicitly meant by saying "either [...] or"

```
False XOR False = False
True  XOR False = True
False XOR True  = True
True  XOR True  = False
```

## 3. Negated questions are a total linguistical disaster

Probably the most simple boolean operator is the NOT operator. Taking only one statement as input, the NOT operator returns the inverse of the given statement.


```
NOT False = True
NOT True  = False
```

The same behavior can be seen in our language. On a sunny day...
It is not sunny. (Incorrect)
It is sunny.     (Correct)


It should be noted, however, that NOT doesn't mean that the inverse of the statement is true, but only that the statement's "correctness" is false.

So, that Jake is not the smartest kid in his class, doesn't necessarily mean that he is the dumbest. Just that he's not THE one brightest. He could just as well be the second most brightest.

In language practice, however, it sometimes happens that your conversation partner uses - wheter they know it's name or not - a rhetorical device called Litotes. Litotes means to say something by negating the opposite. The most common example is probably "Not bad.", meaning "Good."{% sidenote '2' '"Not bad." often also means that they expected it to be bad and are surprised that it isn't. But that's a meta-layer of language we do not care about today.'%}



Unfortunately, that's not it with the NOTs in natural language. The "not" inside a question is something that has been annoying me since the time I was able to understand language on a more complex level.{% sidenote '3' "I assume it started annoying me at age 12. When I started having latin lessons in school."%} Let me explain.

*Are you my son?*

Most of you will probably answer "no" to that question. Precisely, because I don't have any children.


*Are you not my son?*

Now what do you answer? No? Yes? Knowing that a not inverts a statement's value, you are probably quick to jump on saying "yes", but from your natural understanding of language you probably have some doubts. And this doubt makes sense...

The problem is that the word "not" can have two (technically even more) different meanings. It could mean the logical NOT - the one we have been discussing so far and which negates a statement - or it could mean what I'll call a *tag not*, so the not in what is called a *tag question* like "Is it not a beautiful day?" A *tag not* doesn't negate the statement.

Often times you can spot a *tag not* by the phrase it is wrapped inside like "isn't it", but else you are probably lost, making the right answer to question "maybe". "Maybe", however, should never be the right answer to a logical question.


## Conclusion

I am not entirely sure what the point of this text is, for it is neither entirely my views on having conversations nor is it a sufficient guide on boolean algebra / digital logic. Either way, I hope you enjoyed the read or{% sidenote '4' "Note, that this is "or" represents an OR not a XOR."%} learned something.