> Programs are meant to be read by humans and only incidentally for computers to execute #Donald Knuth, Turing award

## Steve's point of view 
> Steve - Author of code complete - Jolt award winning book

* Source Code is the only long lasting accurate description of software
* Software construction is the only activity that's guaranteed to be done
* Great Software is created through the thousands of tiny decisions,design,comments and so on.
* Construct the software well the first time , you wont get a chance to do it again.
* Leave the code more pristine than it was.

## Complexity
* Main reason for project failure is around the requirement gathering
* Second reason is poor project planning
* Third reason - code quality

We shall focus on the code quality.


## Why Have Code Conventions 
> Reference Oracle site

* 80% of the lifetime cost of a piece of software goes to maintenance.
* Hardly any software is maintained for its whole life by the original author.
* Code conventions improve the readability of the software, allowing engineers to understand new code more quickly and thoroughly.

### Git commit message style

* Separate subject from body with a blank line
* Limit the subject line to 50 characters
* Capitalize the subject line
* Do not end the subject line with a period
* Use the imperative mood in the subject line
* Wrap the body at 72 characters
* Use the body to explain what and why vs. how

Credits : Please read [this article](http://chris.beams.io/posts/git-commit/) for more in detail take on the commit messages.

### JavaScript

> Reference - Maintainable JavaScript

#### Blank Lines
* Between methods
* Between local variables in a method and its first statement
* Before multi-line or single-line comment
* Between logical sections inside a method to improve readability

#### Naming
> There hardest problem is naming things

* Code involves variables and functions - use camel case
* Understand the domain and use ubiquitous language from the product owner till the end user , as a developer you should also use the same ubiquitous language for naming.

##### Variables and Functions
* Variables should be in camel case and begin with a noun
* Functions should begin with a verb

``` 
// Good
var count = 10
var found = true
var myName = "Nick"

// Bad
var getCount = 10
var isFound = true

// Good 
function getName() {
   return myName
}

// Bad
function name() {
  return myName 
}
```

##### Constants
* All uppercase letters with underscore separators
```
var MAX_COUNT = 10;
```

#### Null
* Do not use to test whether an argument was supplied
* Do not use the uninitialized variable for the value null

```
// Good
var person = null

// Good
function getPerson () {
   if(condition) {
       return new Person('Nick');
   } else {
       return null;
   }
}

// Bad
var person;
if (person != null) {
    doSomething();
}

// Bad
function doSomething(arg1, arg2, arg3, arg4) {
    if (arg1 != null) {
        doSomething();
    }
}
```

#### Undefined
* null === undefined is false
* null == undefined is true
* Prefer to not use undefined in the code.

```
// foo is not declared
var person;
console.log(typeof person); //undefined"
console.log(typeof foo); //undefined
```
#### Object literals & Array Literals
```
// Bad
var book = new Object()
book.title = "Maintainable JavaScript"
book.author = "Nick"

// Bad
var colors = new Array("red", "black", "green")
var numbers = new Array(1,2,3,4)

// Good
var book = {
    title: "Maintainable JavaScript"
    author: "Nick"
}

// Good
var colors = ["red", "black", "blue"]
var numbers = [1, 2, 3, 4]
```

### Comments
* Add comments for difficult to understand code
* Add comments when something is unclear 

#### Single Line comment
* Include space between the two slashes and the text
* Include empty line preceding the comment
```
// Good
if (condition) {
   
    // if you made it here, then all security checks passed
    allowed(); 
}

// Bad - no space & no blank lines
if (condition) {   
    //if you made it here, then all security checks passed
    allowed(); 
}

// Bad - indentation is not good
if (condition) {   
  //if you made it here, then all security checks passed
    allowed(); 
}

```

#### Multi-line comments
* Include empty line preceding the comment
```
/*
This is an sample for multi-line comment
This is second line
*/

/*
 * This is an sample for multi-line comment
 * This is second line
 */

```

#### Documentation comments

* Matches java documentation comments
* All Methods
    * Include a description of the method , expected arguments and possible return values
* All Constructors
    * Comments should include the purpose of the custom type and expected arguments
* All Classes with documented methods
    * Include a description of the method

```
/**
 * Check out https://googlechrome.github.io/sw-toolbox/docs/master/index.html for
 * more info on how to use sw-toolbox to custom configure your service worker.
 *
 * @param {Object} One or more objects that needs to be merged
 * @return {Object} A new merged object
 */
```
### Avoid Global
* This is a generic principle, it is same across all the languages. 
* In JavaScript - is unique in lot ways and one such thing is the global object
* Creating global is considered to be the bad practice .


## Code Level Optimization
> We should forget about small efficiencies, say about 97% of the time : premature optimization is the root of all evil -- Donald Knuth ,Turing award

* Working toward perfection might prevent completion. Complete it first and then perfect it. The part that needs to be perfect is usually small
* Its not about Algorithm selection
* Its not about Design for performance.

### Reasons to be defensive about code level optimization
* Root cause for complexity and code quality
* Results in accidental complexity

### Defensive Approach
* Step 1: Don't worry about optimization , always write a emphasizing , readable , simple and maintainable code
* Step 2: Measure the performance, if performance is not satisfactory
* Step 3: Find the performance hot-spots.
* Step 4: Perform transformations one at a time.
* Step 5: Measure each transformations and rollback the changes that don't work
* Step 6: Repeat until done.

### Steve's Rule for Code optimization

>If you haven't measured , you don't know 

#### Don't Believe)
* Everybody know that this approach is faster than that.
* I read in that book , that this approach is faster than that.
* I applied this optimization on my last project.

## Principles [TODO]

> There are two ways of constructing a software design: One way is to make it so simple that there are obviously no deficiencies, and the other way is to make it so complicated that there are no obvious deficiencies. The first method is far more difficult - Tony Hoare , Turing award

## Culture

> I have chosen to stress in this talk is the following. We shall do a much better programming job, provided that we approach the task with a full appreciation of its tremendous difficulty, provided that we stick to modest and elegant programming languages, provided that we respect the intrinsic limitations of the human mind and approach the task as Very Humble Programmers. #Turing Lecture 1972 	
The Humble Programmer
by
Edsger W. Dijkstra

### Gist of The Humble Programmer - Djkstra [From Code Complete]

* The people who are best at programming are the people who realize how small their brains are.
* The more you learn to compensate for your small brain , the better a programmer will be.
* Humble programmer write code that is easier for themselves and others to understand and that has fewer errors.

### Manage Complexity

* Divide program into manageable size chunks, chunks should be isolated safely to ignore other chunks - this way you can solve anything.
* Do one thing at a time

### Intellectual Honesty

* Refusing to Pretend you are an expert when you are not
* Admitting your mistakes
* Providing realistic schedule estimates
* Providing realistic status reports

### Communication

* Accept the fact that communication is a challenge.
* Programming is communicating with another programmer first and communicating with the computer second

### Laziness

* Deferring an unpleasant task
* Doing an unpleasant task quickly to get it out of the way 

### Read Books
* You cannot possibly learn everything out of your own experience
* Read a book least in two months

### Be agile
> It Is Not the Strongest of the Species that Survives But the Most Adaptable - Charles Darwin

#### Manifesto for Agile Software Development

>We are uncovering better ways of developing
software by doing it and helping others do it.
Through this work we have come to value:

>Individuals and interactions over processes and tools

>Working software over comprehensive documentation

>Customer collaboration over contract negotiation

>Responding to change over following a plan

>That is, while there is value in the items on
the right, we value the items on the left more.

## Misc
### Presentation

* Avoid commented code
* Do not introduce white spaces or new lines
* Remove unused imports


