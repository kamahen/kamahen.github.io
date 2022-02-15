---
title: My First Post
layout: default
---

# {{ page.title }}

Here is some Prolog code:
```prolog
maplist(_Pred, [], []).
maplist(Pred, [X|Xs], [Y|Ys]) :-
    call(Pred, X, Y),
    maplist(Pred, Xs, Ys).
```
or, using single-sided unification:
```prolog
maplist(_Pred, [], Result) => Result = [].
maplist(Pred, [X|Xs], Result) =>
    Result = [Y|Ys],
    call(Pred, X, Y),
    maplist(Pred, Xs, Ys).
```
