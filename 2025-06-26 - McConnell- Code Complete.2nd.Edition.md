---
kindle-sync:
  bookId: "34959"
  title: AppNee.com.Code.Complete.2nd.Edition
  author: Steve McConnell
  highlightsCount: 84
tags:
  - Books
  - tech
---
# Code Complete 2nd Edition
## Metadata
* Author: Steve McConnell

## Highlights
Likewise, for extremely large software projects, planning of a higher order is needed than for projects that are merely large. Capers Jones reports that a software system with one million lines of code requires an average of 69 kinds of documentation (1998). The requirements specification for such a system would typically be about 4000–5000 pages long, and the design documentation can easily be two or three times as extensive as the requirements. It's unlikely that an individual would be able to understand the complete design for a project — location: [513]() ^ref-61095

---
The carpenter's saying, "Measure twice, cut once" is highly relevant to the construction part of software development, which can account for as much as 65 percent of the total project costs. The worst software projects end up doing construction two or three times or more. Doing the most expensive part of the project twice is as bad an idea in software as it is in any other line of work. — location: [575]() ^ref-56293

---
If you emphasize quality at the end of a project, you emphasize system testing. Testing is what many people think of when they think of software quality assurance. Testing, however, is only one part of a complete quality-assurance strategy, and it's not the most influential part. Testing can't detect a flaw such as building the wrong product or building the right product in the wrong way. Such flaws must be worked out — location: [588]() ^ref-9296

---
Some programmers do know how to perform upstream activities, but they don't prepare because they can't resist the urge to begin coding as soon as possible. — location: [627]() ^ref-58971

---
a focus on prerequisites can reduce costs regardless of whether you use an iterative or a sequential approach. Iterative approaches are usually a better option for many reasons, but an iterative approach that ignores prerequisites can end up costing significantly more than a sequential project that pays close attention to prerequisites. — location: [856]() ^ref-43960

---
If your organization isn't sensitive to the importance of doing requirements first, point out that changes at requirements time are much cheaper than changes later. — location: [1020]() ^ref-20126

---
The problem is their suggesting changes so frequently that you can't keep up. Having a built-in procedure for controlling changes makes everyone happy. You're happy because you know that you'll have to work with changes only at specific times. Your customers are happy because they know that you have a plan for handling their input. — location: [1025]() ^ref-23635

---
Without good software architecture, you may have the right problem but the wrong solution. It may be impossible to have successful construction — location: [1102]() ^ref-25405

---
Generally, a well-run project devotes about 10 to 20 percent of its effort and about 20 to 30 percent of its schedule to requirements, architecture, and up-front planning — location: [1368]() ^ref-20720

---
Studies have shown that the programming-language choice affects productivity and code quality in several ways. Programmers are more productive using a familiar language than an unfamiliar one. Data from the Cocomo II estimation model shows that programmers working in a language they've used for three years or more are about 30 percent more productive than programmers with equivalent experience who are new to a language — location: [1503]() ^ref-26814

---
You save time when you don't need to have an awards ceremony every time a C statement does what it's supposed to. Moreover, higher-level languages are more expressive than lower-level languages. Each line of code says more. — location: [1512]() ^ref-63913

---
the late part of the wave, you can plan to spend most of your day steadily writing new functionality. If you're in the early part of the wave, you can assume that you'll spend a sizeable portion of your time trying to figure out your programming language's undocumented features, debugging errors that turn out to be defects in the library code, revising code so that it will work with a new release of some vendor's library, and so on. — location: [1641]() ^ref-56941

---
your programming tools don't have to determine how you think about programming (1981). Gries makes a distinction between programming in a language vs. programming into a language. Programmers who program "in" a language limit their thoughts to constructs that the language directly supports. If the language tools are primitive, the programmer's thoughts will also be primitive. Programmers who program "into" a language first decide what thoughts they want to express, and then they determine how to express those thoughts using the tools provided by their specific language. — location: [1646]() ^ref-30932

---
Understanding the distinction between programming in a language and programming into one is critical to understanding this book. Most of the important programming principles depend not on specific languages but on the way you use them. If your language lacks constructs that you want to use or is prone to other kinds of problems, try to compensate for them. Invent your own coding conventions, standards, class libraries — location: [1670]() ^ref-54174

---
The picture of the software designer deriving his design in a rational, error-free way from a statement of requirements is quite unrealistic. No system has ever been developed in that way, and probably none ever will. Even the small program developments shown in textbooks and papers are unreal. — location: [1753]() ^ref-29561

---
In an ideal world, every system could run instantly, consume zero storage space, use — location: [1785]() ^ref-36410

---
Dijkstra pointed out that no one's skull is really big enough to contain a modern computer program (Dijkstra 1972), which means that we as software developers shouldn't try to cram whole programs into our skulls at once; we should try to organize our programs in such a way that we can safely focus on one part of it at a time. The goal is to minimize the amount of a program you have to think about at any one time. You might think of this as mental juggling— — location: [1859]() ^ref-26730

---
High fan-in. High fan-in refers to having a high number of classes that use a given class. High fan-in implies that a system has been designed to make good use of utility classes at the lower levels in the system — location: [1905]() ^ref-11440

---
Encapsulation picks up where abstraction leaves off. Abstraction says, "You're allowed to look at an object at a high level of detail." Encapsulation says, "Furthermore, you aren't allowed to look at an object at any other level of detail. — location: [2113]() ^ref-31926

---
Object1 requires Object2 to pass it an Object3. This kind of coupling is tighter than Object1 requiring Object2 to pass it only primitive data types because it requires Object2 to know about Object3. — location: [2389]() ^ref-8100

---
Semantic coupling. The most insidious kind of coupling occurs when one module makes use not of some syntactic element of another module but of some semantic knowledge of another module's inner workings. Here are some examples: Module1 passes a control flag to Module2 that tells Module2 what to do. This approach requires Module1 to make assumptions about the internal workings — location: [2393]() ^ref-58986

---
Cohesion refers to how closely all the routines in a class or all the code in a routine support a central purpose—how focused the class is. — location: [2493]() ^ref-36311

---
and that applies just as well to design. Divide the program into different areas of concern, and then tackle each of those areas individually. If you run into a dead end in one of the areas, iterate! — location: [2617]() ^ref-39556

---
"Top down" and "bottom up" might have an old-fashioned sound, but they provide valuable insight into the creation of object-oriented designs. Top-down design begins at a high level of abstraction. You define base classes or other nonspecific design elements. — location: [2622]() ^ref-6521

---
Bottom-up design starts with specifics and works toward generalities. It typically begins by identifying concrete objects and then generalizes aggregations of objects and base classes from those specifics — location: [2625]() ^ref-63339

---
As you develop the design, you increase the level of detail, identifying derived classes, collaborating classes, and other detailed design elements. Bottom-up design starts with specifics and works toward generalities. It typically begins by identifying concrete objects and then generalizes aggregations of objects and base classes from those specifics. — location: [2624]() ^ref-54675

---
How far do you decompose a program? Continue decomposing until it seems as if it would be easier to code the next level than to decompose it. — location: [2636]() ^ref-60541

---
In the final analysis, top-down and bottom-up design aren't competing strategies— they're mutually beneficial. Design is a heuristic process, which means that no solution is guaranteed to work every time. Design contains elements of trial and error — location: [2668]() ^ref-8394

---
We try to solve the problem by rushing through the design process so that enough time is left at the end of the project to uncover the errors that were made because we rushed through the design process. — Glenford Myers — location: [2714]() ^ref-8039

---
In the twenty-first century, programmers think about programming in terms of classes. A — location: [2920]() ^ref-55501

---
A class is a collection of data and routines that share a cohesive, well-defined responsibility. A class might also be a collection of routines that provides a cohesive set of services even if no common data is involved. A key to being an effective programmer is maximizing the portion of a program that you can safely ignore while working on any one section of code. — location: [2921]() ^ref-60267

---
With an understanding of ADTs, programmers can create classes that are easier to implement initially and easier to modify over time. — location: [2937]() ^ref-41009

---
without encapsulation, abstraction tends to break down. In my experience, either you have both abstraction and encapsulation or you have neither. There is no middle ground. — location: [3291]() ^ref-795

---
Avoid putting private implementation details into a class's interface. With true encapsulation, programmers would not be able to see implementation details at all. They would be hidden both figuratively and literally. — location: [3312]() ^ref-27074

---
Avoid creating god classes. Avoid creating omniscient classes that are all-knowing and all-powerful. If a class spends its time retrieving data from other classes using Get() and Set() routines (that is, digging into their business and telling them what to do), ask whether that functionality might better be organized into those other classes rather than into the god class — location: [3720]() ^ref-12236

---
Eliminate irrelevant classes. If a class consists only of data but no behavior, ask yourself whether it's really a class and consider demoting it — location: [3723]() ^ref-27101

Struct

---
A routine is an individual method or procedure invocable for a single purpose. — location: [3844]() ^ref-17436

---
assigned a value within the routine. The routine has too many parameters. The upper limit for an understandable number of parameters is about 7; this routine has 11. — location: [3880]() ^ref-40783

---
reason to create a routine is to reduce a program's complexity. Create a routine to hide information so that you won't need to think about it. Sure, you'll need to think about it when you write the routine. But after it's written, you should be able to forget the details and use the routine without any knowledge of its internal workings. Other reasons to create routines—minimizing code size, improving maintainability, and improving correctness—are also good reasons, but without the abstractive power of routines, complex programs would be impossible to manage intellectually — location: [3902]() ^ref-31756

---
Giving the test a function of its own emphasizes its significance. It encourages extra effort to make the details of the test readable inside its function. The result is that both the main flow of the code and the test itself become clearer. Simplifying a boolean test is an example of reducing complexity — location: [3939]() ^ref-61282

---
Functional cohesion is the strongest and best kind of cohesion, occurring when a routine performs one and only one operation. Examples of highly cohesive routines include sin(), GetCustomerName(), EraseFile(), CalculateLoanPayment(), and AgeFromBirthdate(). Of course, this evaluation of their cohesion assumes that the routines do what their names say they do—if they do anything else, they are less cohesive and poorly named — location: [4003]() ^ref-60628

---
approximately 50 to 150 lines. In this spirit, IBM once limited routines to 50 lines, and TRW limited them to two pages — location: [4152]() ^ref-23318

---
Don't use routine parameters as working variables. It's dangerous to use the parameters passed to a routine as working variables. Use local variables instead. — location: [4231]() ^ref-9742

---
The input-modify-output convention makes more sense to me, but if you consistently order parameters in some way, you will still do the readers of your code a service. — location: [4194]() ^ref-21403

---
Proponents of the second school argue that the whole object should be passed. They argue that the interface can remain more stable if the called routine has the flexibility to use additional members of the object without changing the routine's interface — location: [4294]() ^ref-36351

---
what abstraction is presented by the routine's interface? If the abstraction is that the routine expects you to have three specific data elements, and it is only a coincidence that those three elements happen to be provided by the same object, then you should pass the three specific data elements individually. However, if the abstraction is that you will always have that particular object in hand and the routine will do something or other with that object, then you truly do break — location: [4298]() ^ref-38321

---
Don't return references or pointers to local data. As soon as the routine ends and the local data goes out of scope, the reference or pointer to the local data will be invalid — location: [4365]() ^ref-60094

---
In defensive programming, the main idea is that if a routine is passed bad data, it won't be hurt, even if the bad data is another routine's fault. — location: [4477]() ^ref-52528

---
A good program uses "garbage in, nothing out," "garbage in, error message out," or "no garbage allowed in" instead. By today's standards, "garbage in, garbage out" is the mark of a sloppy, nonsecure program. — location: [4486]() ^ref-52344

---
Check the values of all data from external sources. When getting data from a file, a user, the network, or some other external interface, check to be sure that the data falls within the allowable range. Make sure that numeric values are within tolerances and that strings are short enough to handle. If a string is intended to represent a restricted range of values (such as a financial transaction ID or something similar), be sure that the string is valid for its intended purpose; otherwise reject it. — location: [4488]() ^ref-41306

---
An assertion is code that's used during development—usually a routine or macro—that allows a program to check itself as it runs. When an assertion is true, that means everything is operating as expected. When it's false, that means it has detected an unexpected error in the code. For example, if the system assumes that a customerinformation file will never have more than 50,000 records, the program might contain an assertion that the number of records is less than or equal to 50,000. — location: [4512]() ^ref-26709

---
use assertions for conditions that should. never occur — location: [4558]() ^ref-23802

---
Handle the error in whatever way works best locally. Some designs call for handling all errors locally—the decision of which specific error-handling method to use is left up to the programmer designing and implementing the part of the system that encounters the error. — location: [4680]() ^ref-60385

404 Page

---
Consumer applications tend to favor robustness to correctness. Any result whatsoever is usually better than the software shutting down. The word processor I'm using occasionally displays a fraction of a line of text at the bottom of the screen. If it detects that condition, do I want the word processor to shut down? No. I know that the next time I hit Page Up or Page Down, — location: [4700]() ^ref-27178

---
Exceptions are a specific means by which code can pass along errors or exceptional events to the code that called it. If code in one routine encounters an unexpected condition that it doesn't know how to handle, it throws an exception, essentially throwing up its hands and yelling, "I don't know what to do about this—I sure hope somebody else knows how to handle it!" Code that has no sense of the context of an error can return control to other parts of the system that might have a better ability to interpret the error and do something useful about it. — location: [4716]() ^ref-61511

---
Throw an exception only for conditions that are truly exceptional. Exceptions should be reserved for conditions that are truly exceptional—in other words, for conditions that cannot be addressed by other coding practices. Exceptions are used in similar circumstances to assertions—for events that are not just infrequent but for events that should never occur — location: [4761]() ^ref-53681

---
Too much defensive programming creates problems of its own. If you check data passed as parameters in every conceivable way in every conceivable place, your program will be fat and slow. What's worse, the additional code needed for defensive programming adds complexity to the software. Code installed for defensive programming is not immune to defects, and you're just as likely to find a defect in defensive-programming code as in any other code— — location: [5035]() ^ref-62934

---
Refactoring. Refactoring is a development approach in which you improve code through a series of semantic preserving transformations. Programmers use patterns of bad code or "smells" to identify sections of code that need to be improved. — location: [5528]() ^ref-17585

---
Code is read far more times than it is written. Be sure that the names you choose favor read-time convenience over write-time convenience. — location: [6987]() ^ref-36541

---
Avoid "magic numbers". Magic numbers are literal numbers, such as 100 or 47524, that appear in the middle of a program without explanation. If you program in a language that supports named constants, use them instead. If you can't use named constants, use global variables when it's feasible to do so. — location: [7013]() ^ref-29598

---
Check for integer overflow. When doing integer multiplication or addition, you need to be aware of the largest possible integer — location: [7061]() ^ref-41641

---
An enumerated type is a type of data that allows each member of a class of objects to be described in English — location: [7330]() ^ref-23127

---
Use enumerated types as an alternative to boolean variables. Often, a boolean variable isn't rich enough to express the meanings it needs to. — location: [7365]() ^ref-29740

---
To appreciate the power of type creation, suppose you're writing a program to convert coordinates in an x, y, z system to latitude, longitude, and elevation. You think that double-precision floating-point numbers might be needed but would prefer to write a program with single-precision floating-point numbers until you're absolutely sure. You can create a new type specifically for coordinates by using a typedef statement in C or C++ or the equivalent in another language. — location: [7549]() ^ref-33943

User obj

---
The term "structure" refers to data that's built up from other types. — location: [7727]() ^ref-25140

---
Use structures to clarify data relationships. Structures bundle groups of related items together. Sometimes the hardest part of figuring out a program is figuring out which data goes with which other data. It's like going to a small town and asking who's related to whom. You come to find out that everybody's kind of related to everybody else, but not really, and you never get a good answer. — location: [7733]() ^ref-59570

---
The location in memory is an address, often expressed in hexadecimal notation. An address on a 32-bit processor would be a 32-bit value, such as 0x0001EA40. The pointer itself contains only this address. To use the data the pointer points to, you have to go to that address and interpret the contents of memory at that location. If you were to look at the memory in that location, it would be just a collection of bits. It has to be interpreted to be meaningful. — location: [7823]() ^ref-61832

---
contents of a location in memory is provided by the base type of the pointer. If a pointer points to an integer, what that really means is that the compiler interprets the memory location given by the pointer as an integer — location: [7828]() ^ref-50884

---
Make sure that you branch correctly on equality. Using > instead of >= or < instead of <= is analogous to making an off-by-one error in accessing an array or computing a loop index. In a loop, think through the endpoints to avoid an off-by-one error. In a conditional statement, think through the equals case to avoid one — location: [8554]() ^ref-10962

---
Put the normal case after the if rather than after the else. Put the case you normally expect to process first. — location: [8557]() ^ref-40425

---
(1)Nominal case. (2)Nominal case. (3)Nominal case. (4)Nominal case. (5)Error case. (6)Error case. (7)Error case. (8)Error case. — location: [8599]() ^ref-12516

---
Order cases by frequency. Put the most frequently executed cases first and the least frequently executed last. — location: [8717]() ^ref-11713

---
Contrary to what some novices think, the test for the loop exit is performed only once each time through the loop, and the main issue with respect to while loops is deciding whether to test at the beginning or the end of the loop. — location: [8899]() ^ref-43782

---
recursion, a routine solves a small part of a problem itself, divides the problem into smaller pieces, and then calls itself to solve each of the smaller pieces. Recursion is usually called into play when a small part of the problem is easy to solve and a large part is easy to decompose into smaller pieces. — location: [9484]() ^ref-1924

---
How do you write a program to find its way through the maze, as shown in Figure 17-1? If you use recursion, the answer is fairly straightforward. You start at the beginning and then try all possible paths until you find your way out of the maze. The first time you visit a point, you try to move left. If you can't move left, you try to go up or down, and if you can't go up or down, you try to go right. You don't have to worry about getting lost — location: [9501]() ^ref-42353

Visited array

---
Make sure the recursion stops. Check the routine to make sure that it includes a nonrecursive path. That usually means that the routine has a test that stops further recursion when it's not needed. — location: [9533]() ^ref-25678

---
Don't use recursion for factorials or Fibonacci numbers. One problem with computer-science textbooks is that they present silly examples of recursion. The typical examples are computing a factorial or computing a Fibonacci sequence. — location: [9557]() ^ref-18341

Memoization

---
Writing test cases before writing the code doesn't take any more effort than writing test cases after the code; it simply resequences the test-case-writing activity. When you write test cases first, you detect defects earlier and you can correct them more easily. — location: [12051]() ^ref-48795

---
Don't trust line numbers in compiler messages. When your compiler reports a mysterious syntax error, look immediately before and immediately after the error—the compiler could have misunderstood — location: [13126]() ^ref-36562

---
A programmer who unintentionally used both the variable SYSTSTS and the variable SYSSTSTS thought he was using a single variable. — location: [13266]() ^ref-13036

---
As you debug, be ready for the problems caused by insufficient psychological distance between similar variable names and between similar routine names. As you construct code, choose names with large differences so that you avoid the problem. — location: [13312]() ^ref-5565

---
Myth: a well-managed software project conducts methodical requirements development and defines a stable list of the program's responsibilities. Design follows requirements, and it is done carefully so that coding can proceed linearly, from start to finish, implying that most of the code can be written once, tested, and forgotten — location: [13449]() ^ref-21721

---
The Pareto Principle, also known as the 80/20 rule, states that you can get 80 percent of the result with 20 percent of the effort. — location: [14060]() ^ref-16820

---
