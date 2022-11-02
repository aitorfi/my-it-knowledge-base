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


## Use Descriptive Names

> Don't be afraid to make a name long. A long descriptive name is better than a short enigmatic name. A long descriptive name is better than a long descriptive comment.
> 
> \- Robert C. Martin, Clean Code (page 39)


## Function Arguments

> The ideal number of arguments for a function is zero (niladic). Next comes one (monadic), followed closely by two (dyadic). Three arguments (triadic) should be avoided where possible. More than three (polyadic) requires very special justification - and then shouldn't be used anyway.
> 
> \- Robert C. Martin, Clean Code (page 40)

> Arguments are even harder from a testing point of view. Imagine the difficulty of writing all the test cases to ensure that all the various combinations of arguments work properly. If there are no arguments this is trivial. If there's one argument, it's not too hard. With two arguments the problem gets a bit more challenging. With more than two arguments, testing every combination of appropriate values can be daunting.
> 
> \- Robert C. Martin, Clean Code (page 40)

### Common Monadic Forms

> There are two very common reasons to pass a single argument into a function. You may be asking a question about that argument, as in `boolean fileExists("MyFile")`. Or you may be operating on that argument, transforming it into something else and *returning it*. For example, `InputStream fileOpen("MyFile")` transforms a file name `String` into an `InputStream` return value. These two uses are what readers expect when they see a function.
> 
> \- Robert C. Martin, Clean Code (page 41)

> A somewhat less common, but still very useful form of a single argument function, is an *event*. In this form there is an input argument but no output argument. The overall program is meant to interpret the function call as an event and use the argument to alter the state of the system, for example, `void passwordAttemptFailedNTimes(int attempts)`. Use this form with care. It should be very clear to the reader that this is an event.
> 
> \- Robert C. Martin, Clean Code (page 41)

### Flag Arguments

> Flag arguments are ugly. Passing a boolean into a function is a truly terrible practice. It immediately complicates the signature of the method, loudly proclaiming that this function does more than one thing, It does one thing if the flag is true and another if the flag is false!
> 
> \- Robert C. Martin, Clean Code (page 41)