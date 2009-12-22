% Continuations
% Josef Svenningsson
%

I'll start out by writing in Markdown. I will have to switch to Latex at some
point since Markdown doesn't support Chapters.

# Introduction

Chapters

* Continuations
* Control Operators
  * callcc
  * shift/reset
  * Felleisens all weird ones
* Continuation Passing Style
* Types and Continuations
* Compiling with Continuations
  * Intermediate language
* Continuations in Logic
* Continuations and Natural Language

# Compilation and Continuation

When writing a compiler one of the central design decisions concerns
the intermediate language (IL), especially for optimizing compilers. 

Using an IL in continuation passing style was a very popular choice
from the late 70's to the early 90's.

Criterions for an intermediate language:

* Simple semantics. Since the IL is where many optimizations happen it is
  crucial that the correctness of these is as simple as possible.

* Simple cost model. When optimizing it is important to know what
  transformations will improve the program and which will have a
  detrimental effect on the speed

* Map relatively easily to the target platform. The IL is, just as it name
  says, an intermediate format which will eventually be translated to 
  something which is platform specific.

* Few constructions. The IL have to be small in order to make it feasible to
  work with.

Some of these criterion are in conflict with each other. To design a
very small intermediate language one might have very powerful language
constructs which can do several tasks at once. But that might be
rather complicated to map to the target platform efficiently, not to
mention that it might complicate the cost model.

# Continuations and Logic

First an introduction to the Curry-Howard isomorphism. There's little need
to talk about intuitionism here so I won't talk about BHK-interpretation. Proof trees as lambda terms. Initially C-H only applied to intuitionistic propositional calculus. In order to deal with classical logic we need to introduce continuations.

But it all really started with the Gödel translation, mapping every classical proof into a proof in intuitionistic logic. This explanation should come after introducing C-H. Apparently both Gödel and Gentzen proved this. But I also have a recollection that there have been other people proving this, perhaps Kolmogorov.

# Continuations and Natural Languages

* Montague semantics of natural language.

* I should read Chris Barker's and Ken Shan's papers.
