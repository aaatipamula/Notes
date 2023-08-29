# Overview

A *proposition* is a declarative sentence that is either *true* ($T$) or *false* ($F$). 

## Logical Operators

These include the following:
-  Negation | *OR* | $\neg$

# Predicates and Quantifiers

## Predicates

Predicates become [[Propositional Logic]] (with truth values) when their vairables are replaced by a value in the *domain* (bound by a [[#Quanifiers:]]).

$P(x)$ is said to be the value of  the Predicate *P at x*.

*Domain* is often noted by $U$.

e.g.  let $P(x)$ denote *x>0*

$P(1)$ -> True
$P(0)$ -> False
$P(3)$ -> True

> The domain $U$ would be any integer

Predicates may also be used with [[#Logical Operators]].

e.g.  let $P(x)$ denote *x>0*

$P(3)\lor P(-1)$ -> True
$P(3)\land P(-1)$ -> False
$P(3)\rightarrow\neg P(-1)$ -> True

Expressions with variables ($P(x)\rightarrow P(2)$) are not propositons and do not have truth values.

## Quantifiers

Quantifiers express the meaning of the words "all" and "some".

The two most important ones are 
- *Universal Quantifier* | "For All" | $\forall$
- *Exestential Quantifier* | "There Exists" | $\exists$