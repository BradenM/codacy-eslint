Labeled statements in JavaScript are used in conjunction with break and continue to control flow around multiple loops. For example:

```
outer:
    while (true) {

        while (true) {
            break outer;
        }
    }
```

The break outer statement ensures that this code will not result in an infinite loop because control is returned to the next statement after the outer label was applied. If this statement was changed to be just break, control would flow back to the outer while statement and an infinite loop would result.
While convenient in some cases, labels tend to be used only rarely and are frowned upon by some as a remedial form of flow control that is more error prone and harder to understand.

This rule aims to eliminate the use of labeled statements in JavaScript. It will warn whenever a labeled statement is encountered and whenever break or continue are used with a label.

[Source](http://eslint.org/docs/rules/no-labels)
