---
title: My wonderful "hello world" page
layout: default
---

# {{ page.title }}

Content is written in [Markdown](https://learnxinyminutes.com/docs/markdown/).
Plain text format allows you to focus on your **content**.

<!--
You can use HTML elements in Markdown, such as the comment element, and they won't
be affected by a markdown parser. However, if you create an HTML element in your
markdown file, you cannot use markdown syntax within that element's contents.
-->

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
