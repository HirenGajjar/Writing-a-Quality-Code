# Writing-a-Quality-Code
The following repo is a result of research on the internet regarding writing of higher quality with the best industry standards.

Hiren Gajjar
Repo Link https://github.com/HirenGajjar/Writing-a-Quality-Code
***


The quality of code can be improved in many ways, but two of the most important ways to do so are the use of common sense and avoiding technically complex writing.

- As the first article from Stack Overflow suggests:
### Article Link: https://stackoverflow.blog/2023/02/13/coding-102-writing-code-other-people-can-read/

Higher-quality code means lower costs. How? Better code improves readability and reduces debugging time.

***Everyone can write better code by:***

~~Using names thoughtfully.~~
1. Using names thoughtfully
2. Using necessary comments
3. Building small functions with severely limited functionalities

- The second article from InformIT suggests:
### Article Link: https://www.informit.com/articles/article.aspx?p=2223710

**Diomidis Spinellis** Wrote a book called ***Code Quality: The Open Source Perspective***

1. Maintain consistency throughout the code
2. Effectively use DSA (Data Structures and Algorithms) to avoid repetition
3. Do not overdesign

- The third article from MetaBox suggests:
### Article Link: https://metabox.io/php-technique-write-clean-readable-code/

***Why coders should focus on clean code, especially in PHP, for certain reasons:***

1. Clean code takes less time to read and write; therefore, not only coders but others can read it and have a basic understanding of it
2. Use documentation while coding so that organizations or others can use it
3. While working on WordPress or other open-source projects that may have strict coding rules, having good practice in producing quality code can definitely help.

For example, WordPress asks to write the full PHP tag as follows:

```PHP
<?php echo 'Hello World'; ?>
```
However, an updated version like 5.4 allows for short tags:

```PHP
<?= 'Hello World'; ?>
```

- Last but not least, an article from Soulimaneyh on Medium suggests:
### Article Link: https://medium.com/@soulaimaneyh/php-clean-code-tricks-everyone-should-know-afd406bd00bc#:~:text=Consistency%20is%20key%20when%20it,lengths%2C%20and%20other%20formatting%20conventions

***PHP, as a language, offers many features and tools to write effectively.***
Here's how?

1. Follow standards like PSR-1 and PSR-2 for indications, line length, and formation
2. Use default functions provided by PHP, such as array_filter(), array_insert(), etc
3. Utilize open-source libraries like CORS, Tinker, and Entrust

---

# Summary
- Naming conventions, comments, and precise functions
- Be consistent, avoid repetition, and be specific when building features
- Code should be written in a way that helps others understand it; documentation and following higher standards can help in open-source contributions

#### > [!Evaluating Work]
> As part of my research, I believe that the above-mentioned articles have been well-structured and summarized.
***3 on the scale out of 4.***



# Code Review

## Missing Elements from Jose Antony's Code Review List

1. The function length should be viewable within a single screen, or in other words, a function's length should not exceed 40 lines
2. Initialize variables of a function before using them within the function
3. During comparison, use constants on the left side of the condition instead of the right side
    - Example 

    ```PHP
    if($value == 2) // Avoid such practices

    if (2 == $variable) // Better approach
    ```

## Check list from nerandell's repo


# General
  - [X] The code works
  - [X] The code is easy to understand
  - [X] Follows coding conventions
  - [X] Names are simple and if possible short
  - [X] Names are spelt correctly
  - [ ] Names contain units where applicable
  - [ ] There are no usages of [magic numbers](http://c2.com/cgi/wiki?MagicNumber)
  - [X] No hard coded constants that could possibly change in the future
  - [ ] All variables are in the smallest scope possible
  - [ ] There is no commented out code
  - [ ] There is no dead code (inaccessible at Runtime)
  - [ ] No code that can be replaced with library functions
  - [ ] Variables are not accidentally used with null values
  - [ ] Variables are immutable where possible
  - [X] Code is not repeated or duplicated
  - [ ] No complex/long boolean expressions
  - [ ] No negatively named boolean variables
  - [ ] No empty blocks of code
  - [ ] Ideal data structures are used
  - [ ] Constructors do not accept null/none values
  - [ ] Catch clauses are fine grained and catch specific exceptions
  - [ ] Exceptions are not eaten if caught, unless explicitly documented otherwise
  - [ ] Files/Sockets and other resources are properly closed even when an exception occurs in using them
  - [ ] `null` is not returned from any method
  - [ ] == operator and === (and its inverse !==) are not mixed up
  - [ ] Floating point numbers are not compared for equality
  - [ ] Loops have a set length and correct termination conditions
  - [X] Blocks of code inside loops are as small as possible
  - [ ] No methods with boolean parameters
  - [ ] No object exists longer than necessary
  - [ ] No memory leaks
  - [ ] Code is unit testable
  - [ ] Test cases are written wherever possible
  - [ ] Methods return early without compromising code readability
  - [ ] Performance is considered
  - [ ] Loop iteration and off by one are taken care of

# Architecture
  - [ ] Design patterns if used are correctly applied
  - [ ] [Law of Demeter](https://en.wikipedia.org/wiki/Law_of_Demeter) is not violated
  - [ ] A class should have only a single responsibility (i.e. only one potential change in the software's specification should be able to affect the specification of the class)
  - [ ] Classes, modules, functions, etc. should be open for extension, but closed for modification
  - [ ] Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program
  - [ ] Many client-specific interfaces are better than one general-purpose interface.
  - [ ] Depend upon Abstractions. Do not depend upon concretions.

# API
  - [ ] APIs and other public contracts check input values and fail fast
  - [ ] API checks for correct oauth scope / user permissions
  - [ ] Any API change should be reflected in the API documentation
  - [ ] APIs return correct status codes in responses

# Logging
  - [ ] Logging should be easily discoverable
  - [ ] Required logs are present
  - [ ] Frivolous logs are absent
  - [ ] Debugging code is absent
  - [ ] No `print_r`, `var_dump` or similar calls exist
  - [ ] No stack traces are printed
  
# Documentation
  - [X] Comments should indicate WHY rather that WHAT the code is doing
  - [X] All methods are commented in clear language.
  - [ ] Comments exist and describe rationale or reasons for decisions in code
  - [ ] All public methods/interfaces/contracts are commented describing usage
  - [ ] All edge cases are described in comments
  - [ ] All unusual behaviour or edge case handling is commented
  - [ ] Data structures and units of measurement are explained


# Security
  - [ ] All data inputs are checked (for the correct type, length/size, format, and range)
  - [ ] Invalid parameter values handled such that exceptions are not thrown
  - [ ] No sensitive information is logged or visible in a stacktrace


*** At this level, memory management, exception handling, garbage collection, APIs, and certain OOP concepts are too much to consider. *** 

### nerandell's checklist has covered all the points from beginner level to expert level programming, whereas Jose Antony's code review is useful for kickstarting. 

#### The reviesed checklist

- Naming conventions, comments, and precise functions
- Be consistent, avoid repetition, and be specific when building features
- Code should be written in a way that helps others understand it; documentation and following higher standards can help in open-source          contributions
- Avoid bad code and do not hide with good comments
- Limit the function length
- Initialize variables of a function before using them within the function
- During comparison, use constants on the left side of the condition instead of the right side


#### > Evaluating work 
*** 3 on the scale out of 4. ***