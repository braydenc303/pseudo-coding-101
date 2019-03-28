
# Pseudocoding 101

Many people that struggle with learning to program need review on how to translate English into both math, and their programming language. This series intends to help you understand very specifically how to take what is said, or given to you in written form and build a mathematical function that you can then use to build your solution on. Think of this as Pseudo-coding 101.

However, in order to get to Pseudocoding, we need to take a few steps first. We will begin with English and figure out how to translate that into math so that we can solve a specific problem. Once we can do that, we will then learn how to write an algorithm to solve many versions of a problem. Finally, we will take our algorithm and turn that into pseudocode.

## Mathematical and Programming Vocabulary

---

We should first begin by discussing how we might interpret spoken or written instructions into mathematical and programming operations.

1. Mathematical Operators in English:
    - __Addition:__
      - increased by
      - more
      - combined, together
      - total of, balance
      - sum, plus
      - added to
      - received
      - deposit
      - comparatives ("greater than", etc)

    - __Subtraction:__
      - decreased by
      - take(n) away, give(n)/gave away
      - minus, less, fewer
      - difference
      - left, left over, after
      - save (old-fashioned term)
      - withdrawal
      - comparatives ("smaller than", etc)

    - __Multiplication:__
      - of
      - times, multiplied by
      - product
      - increased/decreased by a factor of (this last type can involve both addition or -subtraction and multiplication!)
      - twice, triple, etc
      - each ("they got three each", etc)
      - power
      - per (If a known value, depending upon unknown values.)

    - __Division:__
      - per, a (if an unknown value, depending upon known values.)
      - out of
      - go into
      - ratio, quotient
      - fraction, portion, part
      - percent (divide by 100)
      - equal pieces, split
      - average, mean, mode
      - denominator
      - each ("how much does each cost", etc)
      - remainder

    - __Modulus:__
      - remainder
      - left, left over, after

    - __Equals:__
      - is, are, was, were, will be
      - gives, yields, results
      - have, has
      - sold for, cost, price
      - how many

2. English words that hint at how to go about something in Programming:
    - Loops
      - time
      - each
      - next
      - until
      - for
      - while
      - during
      - cycle
      - array

    - if/else statements
      - if (not)
      - and
      - or
      - then
      - unless
      - otherwise

Once we have a basic understanding of what needs to be accomplished, we can start making a list of what values and variables we might need. Start off with the values that we know, then go on to name the variables of information that you wish to determine later.

For example. If we have a word problem like this:

>If Peter Piper picked 8 pecks of pickled peppers, how many peppers did Peter Piper pick? Keep in mind that one peck is equal to 8 quarts. Let's also assume that the peppers were pepperoncinis, and that there are 15 pepperoncinis per quart.

We could list out our known values like this:

>pecks = 8
>
>quart/peck conversion factor: 8 quarts/peck
>
>pepper/quart conversion factor 15 peppers/quart

Our unknowns would be:

>Total peppers

Perhaps more succinctly:

| knowns          | unknowns |
|-----------------|----------|
|pecks = 8        |  total   |
|quart2peck = 8   |          |
|pepper2quart = 15|          |

Now to write out our equation:

>8 pecks(8 quarts/peck * 15 peppers/quart) = total

If we now follow our order of operations we first multiply the values in parenthesis, and see that we get:

>120 peppers/peck
>
>Times 8 pecks
>
>960 peppers = total

So when it comes to pseudocoding and programming, what should we name our variables? First let's start with what we can name our varibles.

Every programming language has a set of conventions for naming variables. We are going to use JavaScript as an example for what we need to take into consideration when naming variables in an algorithm. Please refer to documentation/guidlines for the language(s) that you are programming in.

- JavaScript

  - Variable names can include any letter, number, or underscore. No other characters or spaces.

  - Keep in mind that names are case sensitive.

  - The first character must be a letter or an underscore.

  - There is no limit to the length.

  - You cannot use any of JavaScript's reserved words, and should avoid the use of many of JavaScript's keywords. [Reference](https://www.w3schools.com/js/js_reserved.asp)
  
    - Reserved Words

      - abstract, arguments, await*, boolean,
        break, byte, case, catch,
        char, class*, const, continue,
        debugger, default, delete, do,
        double, else, enum*, eval,
        export*, extends*, false, final,
        finally, float, for, function,
        goto, if, implements, import*,
        in, instanceof, int, interface,
        let*, long, native, new,
        null, package, private, protected,
        public, return, short, static,
        super*, switch, synchronized, this,
        throw, throws, transient, true,
        try, typeof, var, void,
        volatile, while, with, yield

Because JavaScript is used in conjunction with Java, HTML, and others, you will want to refer to documentation for any languages that you are also working with.

## Writing An Algorithm

---

An algorithm is just a series of step by step instructions. The best example of an algorithm that most people have seen would be the instructions for a recipe.

A good algorithm has a set of inputs, a well defined, finite number of steps, and produces the desired output. Each step should be a simple instruction.

In addition to the above, we need to formalize a few more terms:

---

Arguments: Variables utilized by a function.

Take in: This is used to refer to any specific arguments that your function may have to use.

> ex. Take in num1

Return: Refers to the value of our function result.

Count: Indicates a loop and is also the variable name we will use for the iterator(size of step) of the loop.

---

To begin let's write a very simple algorithm to complete a very simple task.

Write an algorithm that will return the total of two numbers.

```Algorithm
1. Take in num1 and num2

2. total = num1 + num2

3. Return total
```

In the example above, we have a set of inputs, we have a well defined, finite, set of steps, and it produces the desired result.

Now that we can write an algorithm for a very simple task, let's go back to the example we used in our word problem above. But instead of simply solving the problem, let's write an algorithm to do so.

>If Peter Piper picked 8 pecks of pickled peppers, how many peppers did Peter Piper pick? Keep in mind that one peck is equal to 8 quarts. Let's also assume that the peppers were pepperoncinis, and that there are 15 pepperoncinis per quart.

```Algorithm
1. Take in the number of pecks Peter Piper picked, the conversion from pecks to quarts, and the conversion from quarts to peppers.

2. Multiply the two conversion factors to determine how many peppers per peck.

3. Multiply the number of pecks Peter Piper picked by the peppers per peck conversion.

4. Return the total
```

Now we have an algorithm that can solve for the total number of peppers no matter how many pecks that Peter Piper might pick.

It is now time to add more complexity to our algorithms. Here we will be looking at loops and conditionals. Loops are instructions that are done repeatedly, and conditionals are instructions that are performed only when a certain condition is true. Conditional instructions can also include multiple cases in which we would include an "else".

Before we actually write an algorithm including a loop or conditional however, let's outline how those things are written.

### Loops

For loops, we need a few pieces of information. We need a place to start, a place to end, and how large of a step or increment to take each time. In writing an algorithm, the instructions for a generic loop would look something like this:

```Algorithm
1. Count from x to y in increments of 1
2. Each time, do something
```

Write an algorithm that will return the numbers from one to some number one at a time.

```Algorithm
1. Take in num1
1. Count from 1 to num1 in increments of 1.
2. Each time, return count.
```

### Conditionals

For a conditional instruction, we also need a few pieces of information. We need to know what the condition that needs to be met for a given instruction might be, as well as if there is something else that we should do if conditions are different, or if we should just continue on. We would write a conditional instruction like this:

```Algorithm
1. If (condition) do something.
2. Else if (condition) do something else.
3. Else continue.
```

In order to demonstrate a conditional statement, we are going to combine it with a conditional statement just for the sake of practice.

Write an algorithm that will return all of the even numbers between 1 and some number.

```Algorithm
1. Take in num1
2. Count from 1 to num1 in increments of 1
3. Each time, if count is evenly divisible by 2, return count
```

Now that have covered all the basics, of how to write an algorithm, let's see if we can apply what we know to one of the staple whiteboarding problems in the programming community: FizzBuzz.

FizzBuzz goes something like this.

Write an algorithm that will return "Fizz" if a number is divisible by 3, "Buzz" if a number is divisible by 5, and "FizzBuzz" if divisible by both. Otherwise, just return the number, from 1 to some number.

As always our first step will be to take in any needed inputs. Then we can run through our other steps.

1. Take in num1.

2. Count from 1 to num1 in increments of 1.

3. Each time:

    a. If count is evenly divisible by 3 and 5, return "FizzBuzz"

    b. If count is evenly divisible by 3, return "Fizz"

    c. If count is evenly divisible by 5, return "Buzz"

    d. Else return count

Remember, that our instructions must be as simple as possible. Meaning that each time we go through the loop, we will only pass one of the tests, and if we do, we are done with that turn in the loop. If that is the case, this algorithm will only work because it is written in this particular order.

With the steps written in this order, we will test each number to see if it is evenly divisible by 3 and 5. If it is, we will return "FizzBuzz". If not, we will then test if the number is evenly divisible by 3. If so, we will return "Fizz". If not, we will test to see if the number is evenly divisible by 5. If so, we will return "Buzz". Then if the number is not evenly divisible by either 3 or 5, we will return the number.

If we had instead written the step in 3a after b and c in the order of tests, we never would have gotten to it because we would have passed one of those tests first and ended that turn in the loop. So we would have seen "Fizz" for all numbers only divisible by 3, as well as numbers divisible by 3 and 5 because we would pass the first test for numbers divisible by 3. We would then see "Buzz" for all numbers only divisible by 5, and of course all remaining numbers would just be returned. Without us ever hitting the test for numbers divisible by 3 and 5, we would never see "FizzBuzz".

## Pseudocoding

---

Pseudocoding uses the structural conventions of a normal programming language, but is intended more readable by a person. Its really just a step in between writing an algorithm, and writing a program in a specific language.

Like in a programming language we will be pseudocoding functions. However, we will have a shift from the more explicit language of writing algorithms, to a greater use of mathematical operators, and brackets.

To make our lives a little easier, let's outline the meaning that each of the different brackets carry?

- ( ) Do this first, Take in argument(s), use this.
- { } Steps of a function, values in an object.
- [ ] An index/address in an array.

Just for fun, if we were to pseudocode out our tongue twister from above, it might look something like this:

```Pseudocode
  function(pecks) {
    total = pecks(8 quarts/peck * 15 peppers/quart)
    return total
  }
```

Write a function that will return all numbers from 1 to some number.

```Pseudocode
function(num1) {
  for(count = 1; count <= 1; count = count + 1) {
    return count;
  }
}
```

Write a function that will return all even numbers from 1 to some number.

```Pseudocode
function(num1) {
  for(count = 1; count <= 1; count = count + 1) {
    If count is evenly divisible by 2 {
      return count
    }
  }
}
```

Now let's see what it would look like if we were to apply this format to our old friend FizzBuzz.

Write an algorithm that will return "Fizz" if a number is divisible by 3, "Buzz" if a number is divisible by 5, and "FizzBuzz" if divisible by both. Otherwise, just return the number, from 1 to some number.

```Pseudocode
function(num1) {
  for(count = 1; count<= 1; count = count + 1) {
    If count is evenly divisible by 3 and 5 return "FizzBuzz"
    Else if count is evenly divisible by 3 return "Fizz"
    Else if count is evenly divisible by 5 return "Buzz"
    Else return count
  }
}
```

We have covered a lot of ground here. I hope that this can help those new to coding learn programming concepts more clearly, as well as more quickly.