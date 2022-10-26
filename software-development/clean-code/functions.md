# Functions
@see [Meaningful Names](./meaningful-names.md)

## Blocks and Indenting

> ...the blocks within `if` statements, `else` statements, `while` statements, and so on should be one line long. Probably that line should be a function call. Not only does this keep the enclosing function small, but it also adds documentary value because the function called within the block can have a nicely descriptive name.
> 
> This also implies that function should not be large enough to hold nested structures. Therefore, the indent level of a function should not be greater than one or two. This, of course, makes the functions easier to read and understand.
> 
> \- Robert C. Martin, Clean Code (pages 35)


## One Level of Abstraction per Function

> In order to make sure our functions are doing "one thing", we need to make sure that the statements within our function are all at the same level of abstraction.
> ...
> Mixing levels of abstraction within a function is always confusing. Readers may not be able to tell whether a particular expression is an essential concept or a detail.
> 
> \- Robert C. Martin, Clean Code (pages 36)