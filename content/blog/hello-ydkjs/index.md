---
title: Hello YDKJS Up & Going!
date: "2020-10-07T02:32:37.121Z"
---
```Day #1``` 
---
```date: 2020-10-07```

## Motivation
Second attempt and focussing on reading this you don't know JS book for understanding the in and outs of the mysterious language. The truth to wizardry is just by following the spells and practice them a million times.


At the end you don't aim to just copy snippets from stackoverflow but aim to write clean, engineered and scalable code.

The absurdaties such as objects, closures, scopes and other jargons will actually make sense once we start learning js!


### Chapter 1

`Into programming`  The most basic topic of the lot with basic explanation on type conversions and giving an overview on how programming languages work whilst pinning the design patterns and the flavour of JS.

The topics covered are basic for a developer and don't require too much attention as they are fairly the same in all the other languages. 

### Chapter 2

`Into JS` 

 


 
Truthy and falsy values.

#### Equality are of two levels. Strict and loose.

!==  vs === is just that == allows coercision and one does not! It's easy to pinpoint explicit coercisions as they are intended by the developer whereas implicit coercisions take developers by surprise as they are heavily dependent on the context of the code which might sometimes a blind spot for the developer.


>var a = "42";

>var b = a * 1;

>a ; // "42"

>b ; // 42 ....Number


If you try to access a variable's value in a scope where it's not available, you'll get a ReferenceError thrown.

Function scopes .
Nested function scopes.
Global declaration without def


<!-- title: Hello JS! -->
``` Day #2 ```
---
```date: 2020-09-05```

As Js isn't forward compatible, we may run into error or break the app if we use a ```ES2019``` feature in an ```engine from 2016```

If the new feature is a new syntax then it will fail sooner or later and may even pop a runtime exception if its an API !

The solution is transpiling, its the process of converting new syntax to  old format syntax using transpiler, eg: [Babel](https://babeljs.io). 


### console.log(isJS.Interpreted()) ?

The following is a snippet from the book `You don't know JS by Kyle ` [Link](https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#whats-in-an-interpretation)
>In scripted or interpreted languages, an error on line 5 of a program won't be discovered until lines 1 through 4 have already executed. Notably, the error on line 5 might be due to a runtime condition, such as some variable or value having an unsuitable value for an operation, or it may be due to a malformed statement/command on that line. Depending on context, deferring error handling to the line the error occurs on may be a desirable or undesirable effect.

>Compare that to languages which do go through a processing step (typically, called parsing) before any execution occurs, as illustrated in Figure 2:

>Parsing, compiling, and executing a program
![Figure-2](https://raw.githubusercontent.com/getify/You-Dont-Know-JS/2nd-ed/get-started/images/fig2.svg)
>Fig. 2: Parsing + Compilation + Execution

>In this processing model, an invalid command (such as broken syntax) on line 5 would be caught during the parsing phase, before any execution has begun, and none of the program would run. For catching syntax (or otherwise "static") errors, generally it's preferred to know about them ahead of any doomed partial execution.

>So what do "parsed" languages have in common with "compiled" languages? First, all compiled languages are parsed. So a parsed language is quite a ways down the road toward being compiled already. In classic compilation theory, the last remaining step after parsing is code generation: producing an executable form.

>Once any source program has been fully parsed, it's very common that its subsequent execution will, in some form or fashion, > a translation from the parsed form of the program—usually called an Abstract Syntax Tree (AST)—to that executable form.

>In other words, parsed languages usually also perform code generation before execution, so it's not that much of a stretch to say that, in spirit, they're compiled languages.

>JS source code is parsed before it is executed. The specification requires as much, because it calls for "early errors"—statically determined errors in code, such as a duplicate parameter name—to be reported before the code starts executing. Those errors cannot be recognized without the code having been parsed.

>So JS is a parsed language, but is it compiled?

>The answer is closer to yes than no. The parsed JS is converted to an optimized (binary) form, and that "code" is subsequently executed (Figure 2); the engine does not commonly switch back into line-by-line execution (like Figure 1) mode after it has finished all the hard work of parsing—most languages/engines wouldn't, because that would be highly inefficient.

>To be specific, this "compilation" produces a binary byte code (of sorts), which is then handed to the "JS virtual machine" to execute. Some like to say this VM is "interpreting" the byte code. But then that means Java, and a dozen other JVM-driven languages, for that matter, are interpreted rather than compiled. Of course, that contradicts the typical assertion that Java/etc are compiled languages.

>Interestingly, while Java and JavaScript are very different languages, the question of interpreted/compiled is pretty closely related between them!

>Another wrinkle is that JS engines can employ multiple passes of JIT (Just-In-Time) processing/optimization on the generated code (post parsing), which again could reasonably be labeled either "compilation" or "interpretation" depending on perspective. It's actually a fantastically complex situation under the hood of a JS engine.

>So what do these nitty-gritty details boil down to? Step back and consider the entire flow of a JS source program:

>After a program leaves a developer's editor, it gets transpiled by Babel, then packed by Webpack (and perhaps half a dozen other build processes), then it gets delivered in that very different form to a JS engine.

>The JS engine parses the code to an AST.

>Then the engine converts that AST to a kind-of byte code, a binary intermediate representation (IR), which is then refined/converted even further by the optimizing JIT compiler.

>Finally, the JS VM executes the program.
![Figure-3](https://raw.githubusercontent.com/getify/You-Dont-Know-JS/74a7f6ab97198da2d20be135c63bedf2c853bfb0/get-started/images/fig3.svg)

>I think it's clear that in spirit, if not in practice, JS is a compiled language.
([Wikipedia Link](https://en.wikipedia.org/wiki/Salted_duck_egg))

Yeah, I didn't either.
