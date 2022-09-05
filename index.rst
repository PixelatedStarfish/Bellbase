====
Bellbase
====

.. container:: noprint
   :name: mw-page-base

.. container:: noprint
   :name: mw-head-base

.. container:: mw-body
   :name: content

   .. container:: mw-body-content
      :name: siteNotice

   .. container:: mw-indicators mw-body-content

   .. rubric:: 
   
      :name: firstHeading
      :class: firstHeading

   .. container:: mw-body-content
      :name: bodyContent

      .. container::
         :name: contentSub

      .. container::
         :name: contentSub2

      .. container::
         :name: jump-to-nav

      .. container:: mw-content-ltr
         :name: mw-content-text

         .. container:: mw-parser-output

            | 

            .. container:: mw-content-ltr
               :name: mw-content-text

               .. container:: mw-parser-output

                  | 
                  | Bellbase is a programming language created by
                    PixelatedStarfish in 2022 and it is designed to be a
                    simple, practical language for learning to program.

                  Bellbase was initially created as a second major
                  version of MacroBeep, designed to support subroutines.
                  MacroBeep v2.0 diverged to the point where it was best
                  renamed, as a new language entirely.

                  The current version is version 1.2 and the language
                  file extension is ``.bbe``

                  | 

                  .. container:: toc
                     :name: toc

                     .. container:: toctitle

                        .. rubric:: Contents
                           :name: mw-toc-heading

                     -  `1 Design Goals: Why Use
                        Bellbase? <#Design_Goals:_Why_Use_Bellbase.3F>`__
                     -  `2 Factors in Design <#Factors_in_Design>`__

                     -  `3 Influences: Shameless
                        Theft <#Influences:_Shameless_Theft>`__
                     -  `4 Acknowledgements <#Acknowledgements>`__
                     -  `5 Program Examples <#Program_Examples>`__

                     -  `6 Syntax <#Syntax>`__

                     -  `7 Compiling and
                        Interpreting <#Compiling_and_Interpreting>`__
                     -  `8 Variables <#Variables>`__
                     -  `9 Lists, Indexing, and
                        Nesting <#Lists.2C_Indexing.2C_and_Nesting>`__
                     -  `10 Strings and
                        Escapes <#Strings_and_Escapes>`__

                     -  `11 Identifiers: How to Use the Identifying
                        Operator
                        @ <#Identifiers:_How_to_Use_the_Identifying_Operator_.40>`__
                     -  `12 Labels and
                        Conditionals <#Labels_and_Conditionals>`__

                     -  `13 Structs: Defining a Data
                        Type <#Structs:_Defining_a_Data_Type>`__

                     -  `14 Functions <#Functions>`__

                     -  `15 Macros <#Macros>`__

                     -  `16 Files <#Files>`__
                     -  `17 Errors <#Errors>`__

                     -  `18 Commands <#Commands>`__

                     -  `19 Using the
                        Interpreter <#Using_the_Interpreter>`__
                     -  `20 The Linker: Include
                        Commands <#The_Linker:_Include_Commands>`__

                     -  `21 Libraries <#Libraries>`__

                     -  `22 Proof of Turing
                        Completeness <#Proof_of_Turing_Completeness>`__

                     -  `23 Syntax
                        Highlighting <#Syntax_Highlighting>`__

                     -  `24 Interpreter
                        Extensibility <#Interpreter_Extensibility>`__

                     -  `25 Test Cases <#Test_Cases>`__

                     -  `26 Index <#Index>`__

                     -  `27 ASCII Table <#ASCII_Table_2>`__
                     -  `28 Sources <#Sources>`__

                  .. rubric:: Design Goals: Why Use Bellbase?
                     :name: design-goals-why-use-bellbase

                  This language is designed to learn by tinkering. It is
                  designed for students to practice essential
                  programming skills, such as tracing, debugging, and
                  memory management.

                  Someone can learn to code with any programming
                  language, but few are designed for learning, and fewer
                  still are designed for an adult learner. Why is
                  transitioning from a graphical, block-based language,
                  to a text-based one so hard? Well, there are
                  constructs and conventions to memorize. There might
                  even be three different kinds of grouping symbols:
                  (parentheses), [brackets], {braces}. A new programmer
                  has a lot of questions. How do I install this? Which
                  version am I using? How do I do this or that? What is
                  this thing again? What does this error mean? Bellbase
                  is designed to ensure a new programmer can stop
                  stressing, and focus on expressing their programs in
                  code.

                  -  Bellbase has a simplified syntax, for programs that
                     are easier to write, organize, trace, and debug.
                  -  Lexemes are descriptive, such that the tokens they
                     represent are clearly indicated.
                  -  Memory is always bound to function calls, which
                     eliminates confusing design patterns while
                     maintaining usability.

                  .. rubric:: Factors in Design
                     :name: factors-in-design

                  Always write the simplest code you can. Never
                  implement a complicated algorithm when a simple one
                  will do.

                  .. rubric:: On Languages Designed for Pedagogy:
                     Thoughts on Stacking Blocks
                     :name: on-languages-designed-for-pedagogy-thoughts-on-stacking-blocks

                  Many languages with a pedagogical design philosophy
                  are written for children. Such languages typically
                  employ a form of graphics based coding in specialized
                  IDEs (Integrated Development Environments) in which
                  programming is accomplished by clicking and dragging
                  colorful blocks. These blocks have statements written
                  on them and fit together like puzzle pieces. In
                  general, I believe these languages are a success. A
                  child can enjoy programming a video game, or an
                  animated story without dealing with abstract data
                  structures and advanced concepts in object oriented
                  programming. Instinctively, one can learn how to read
                  source code and debug it; how to use loops, variables,
                  and conditional statements. Then it comes time to get
                  bolder, try out some data structures. Code gets long,
                  hundreds, or even thousands of blocks long. The IDE
                  starts to slow and lag. The programmer hits a ceiling,
                  and it comes time to transition to a more efficient
                  language, one that describes source with efficient,
                  computer-friendly text. That is the hard part.

                  Most high-level languages are not based on stacking
                  colorful blocks. They have keywords instead. In a
                  language like Scratch, blocks are commands, or
                  arguments for commands. Even when a block is
                  completely isolated from your program, you can click
                  on it and watch it do something. A cat goes left. A
                  variable is set. A list is emptied. Not all keywords
                  have this property. Many keywords modify groups of
                  statements (which are also called blocks and opened
                  and closed with braces. I call them groups here to
                  avoid confusion.) The if keyword makes this block an
                  if statement. The fn keyword means this group is a
                  function. The private keyword modifies the fn keyword,
                  indicating this function cannot be accessed outside
                  the encapsulating class. Keywords can express abstract
                  syntax, but many do not constitute a serviceable
                  program in isolation. They do not do anything without
                  context. This is one of a few factors that makes
                  transitioning from Scratch to a C-style language hard.

                  Bellbase commands are designed to be at a halfway
                  point between Scratch blocks and C-style keywords.
                  Most commands are programs that operate independent of
                  other commands, in a manner similar to a Scratch
                  block, or a function. However, Bellbase commands are
                  also versatile enough to describe functions, macros,
                  and data structures, in a manner similar to a C-style
                  language.

                  .. rubric:: Clarity: Why no Braces?
                     :name: clarity-why-no-braces

                  Many people like braces.
                  ``from future import __braces__`` is a joke among
                  python programmers. Yes, braces are great for
                  delineating blocks of statements, but they are easily
                  disorganized and do not describe the blocks well.
                  Consider this, often found at the end of a source
                  file:

                  ::

                     }
                       }}
                     }

                  What are they enclosing? Which opening braces do they
                  close? How does deleting one effect source? Nothing is
                  clear about this syntax, a comment is needed for each
                  brace. Something more descriptive is possible:

                  ::

                     struct @foo
                      #statements
                     _struct

                  Even if ``_struct`` is the only statement shown, it is
                  still clear that it describes the end of a struct.

                  .. rubric:: Influences: Shameless Theft
                     :name: influences-shameless-theft

                  -  Structs, Macros, and Includes come from C.
                  -  The command syntax comes from assembly languages
                     like ARM, and block-based languages like Scratch.
                  -  The call trace and data types are adapted from Java
                     (and ultimately, C).
                  -  The format for error messages is adapted from
                     Python.
                  -  Clojure influenced the syntax of functions, such
                     that functions are first class, rather than second
                     class.

                  .. rubric:: Acknowledgements
                     :name: acknowledgements

                  Thank you to the Skidmore College faculty, O'Connell,
                  Dufour, Eckmann, Read, Reiley, and Prasad. I am glad
                  to have my degree in computer science! I would also
                  like to thank Bringas, Kravsky, and Lee for their
                  tutelage, patience, and inspiration. Bellbase would
                  not exist without the esolangs wiki and the work of
                  youtuber User:Truttle1.

                  Thanks to User:Gapples2 for their questions, comments,
                  and insights. This language is better for them.

                  Of course I should thank my loved ones for their
                  support.

                  .. rubric:: Program Examples
                     :name: program-examples

                  .. rubric:: Hello World
                     :name: hello-world

                  Outputs “Hello World” to the console.

                  ::

                     func @main
                      out "Hello World" 
                      return 

                  .. rubric:: Truth Machine
                     :name: truth-machine

                  A problem by User:Keymaker to demonstrate usability.
                  It takes a 0 or a 1. If it gets a 1 it outputs an
                  endless sequence of ones. Otherwise it prints 0.

                  ::

                     func @main
                      int @c (:input "int")
                      beq &c 0 Terminate
                      label @Forever
                       out 1
                       goto Forever
                      label @Terminate
                       out 0
                      return

                  .. rubric:: Cat (Echo)
                     :name: cat-echo

                  Outputs the input given.

                  ::

                     func @main
                      out "Feed the cat\n" 
                      out (:input "string")
                      return 

                  .. rubric:: FizzBuzz
                     :name: fizzbuzz

                  ::

                     include lib/Math/Ops.bbe 

                     func @main
                      char @c
                      int @i 0
                      label @loop
                       beq ((:mod &i 15) 0) FizzBuzz
                       beq ((:mod &i 5) 0) Buzz
                       beq ((:mod &i 3) 0) Fizz
                      goto nonCase

                      label @Fizz
                       out "Fizz\n" 
                      goto loopEnd 

                      label @Buzz
                       out "Buzz\n" 
                      goto loopEnd

                      label @FizzBuzz
                       out "FizzBuzz\n" 
                      goto loopEnd

                      label @nonCase
                       out &i
                       out "\n"

                      label @loopEnd
                       give &i 1
                       bleq &i 100 loop 
                      return 

                  .. rubric:: Syntax
                     :name: syntax

                  .. rubric:: Statements
                     :name: statements

                  Statements are a single line of code that are
                  interpreted to run a program. Each statement starts
                  with a command, which can take arguments. The
                  arguments for a command can be separated by tabs or
                  spaces. A command can also have arbitrary spaces and
                  tabs before it.

                  ::

                     command arg1 arg2 arg3 #etc

                  .. rubric:: Comments
                     :name: comments

                  Comments are not interpreted; they are for
                  programmers, not computers. Comments are indicated
                  with hashes.

                  ::

                     #inline comment

                     ##
                     Multiple
                     Line
                     Comment
                     ##

                  When writing a comment, it is better to explain why
                  the code is there, not what it is for.

                  .. rubric:: Blocks
                     :name: blocks

                  Some commands define blocks of code that group
                  multiple statements together. Here is an example of a
                  data structure with attributes:

                  ::

                     struct @foo
                      int @a
                      string @b
                     _struct

                  Any command that defines a block has a corresponding
                  block ender, which is the starting command preceded by
                  an underscore. The ``struct`` block ends with
                  ``_struct``. ``macro`` ends with ``_macro`` and a
                  ``func`` can end with ``_func`` although it is more
                  common to end a function with ``return``.

                  Blocks cannot nest, nesting blocks throws an error.

                  .. rubric:: Argument Tokens
                     :name: argument-tokens

                  A command can take a few different tokens as
                  arguments:

                  -  An IDENTIFIER identifies something. It is used to
                     create a variable, function, or struct.
                  -  A FUNCTION CALL is a function name preceded by a
                     colon. This call can be passed to a function,
                     returned by a function, or evaluated.
                  -  FUNCTIONS are data and references can be made to
                     them.
                  -  A VAR is an argument that refers to a cell with the
                     refer operator (**&**). Any sequence of refer
                     operators followed by an integer is a VAR.
                  -  A VALUE is any token that can be stored in a
                     variable. These can be NUMBERS (longs, ints,
                     floats, doubles, chars); COLLECTIONS (strings
                     lists, and words); or STRUCTS (a data type defined
                     in source.)
                  -  A LIST is a data type that can store values of
                     multiple types. LISTS are COMPLEX COLLECTIONS, so
                     are STRUCTS and FUNCTIONS.
                  -  A STRING is a sequence of printable characters
                     framed by double quotes. Each string is one
                     argument, even if it includes spaces. A STRING is a
                     SIMPLE COLLECTION, because it can only store data
                     of one type, characters.
                  -  LABELS organize source code.
                  -  PATHS point to files.
                  -  WORDS are the untyped argument. Every argument is a
                     WORD.

                  .. rubric:: Token Order
                     :name: token-order

                  In a statement, tokens take the following order from
                  left to right:

                  -  Commands
                  -  Identifiers
                  -  Function Calls
                  -  Variables and Structs
                  -  Numbers
                  -  Strings
                  -  Lists
                  -  Labels
                  -  Paths

                  .. rubric:: Parentheses and Brackets
                     :name: parentheses-and-brackets

                  (parentheses) and [brackets] are useful for grouping
                  tokens together, but they serve distinct functions in
                  code:

                  -  Parentheses group calls, and the arguments those
                     calls take together.
                  -  Brackets group arguments into a list.

                  To demonstrate syntactic distinction, let ``:foo`` be
                  an arbitrary function that does the following:

                  -  When given a number argument, add 10 to that and
                     return the result.
                  -  Otherwise, return 0.

                  Compare these two lines:

                  ::

                     (:foo 10)
                     [:foo 10]

                  The top line is a call, and it evaluates to ``20``.
                  The bottom one is a list, and it evaluates to
                  ``[0 10]``. An argument is accepted by the function on
                  the top line, but not the bottom one.

                  .. rubric:: Useful Operators
                     :name: useful-operators

                  Some operators appear in multiple tables.

                  .. table:: Argument Specifiers

                     +-----------+----------------------+---------------------------+
                     | Operation | Name                 | Desc.                     |
                     +-----------+----------------------+---------------------------+
                     | ``&``     | Refer                | Refers to a variable.     |
                     +-----------+----------------------+---------------------------+
                     | ``:``     | Call Passing         | Call Passing; Passes a    |
                     |           |                      | function call as an       |
                     |           |                      | argument.                 |
                     +-----------+----------------------+---------------------------+
                     | ``@``     | Identifying Operator | For naming data.          |
                     +-----------+----------------------+---------------------------+
                     | ``"``     | Quote                | Frames a String.          |
                     +-----------+----------------------+---------------------------+
                     | ``(``     | Open Parenthesis     | Starts a parenthetical    |
                     |           |                      | grouping, which evaluates |
                     |           |                      | first.                    |
                     +-----------+----------------------+---------------------------+
                     | ``)``     | Close Parenthesis    | Close Parenthesis; Closes |
                     |           |                      | a parenthetical grouping. |
                     +-----------+----------------------+---------------------------+
                     | ``[``     | Open Bracket         | Open list.                |
                     +-----------+----------------------+---------------------------+
                     | ``]``     | Close Bracket        | Close list.               |
                     +-----------+----------------------+---------------------------+
                     | ``!``     | Bang                 | Macro operator.           |
                     +-----------+----------------------+---------------------------+
                     | ``#``     | Hash                 | Starts inline comment.    |
                     |           |                      | Everything to the right   |
                     |           |                      | is a comment.             |
                     +-----------+----------------------+---------------------------+

                  | 

                  .. table:: Compiler Operators

                     +-----------+------------------------+---------------------------+
                     | Operation | Name                   | Desc.                     |
                     +-----------+------------------------+---------------------------+
                     | ``*``     | Star                   | Gets the contents of a    |
                     |           |                        | directory and load files  |
                     |           |                        | into the linker.          |
                     +-----------+------------------------+---------------------------+
                     | ``->``    | Right Arrow            | This is substituted with  |
                     |           |                        | the path from *bbe* to    |
                     |           |                        | the current file.         |
                     +-----------+------------------------+---------------------------+
                     | ``/``     | Subdirectory Delimiter | Extends path to a         |
                     |           |                        | subdirectory.             |
                     +-----------+------------------------+---------------------------+
                     | ``!``     | Bang                   | Macro operator.           |
                     +-----------+------------------------+---------------------------+

                  | 

                  .. table:: Lexical Operators

                     +-----------+---------------------------+---------------------------+
                     | Operation | Name                      | Desc.                     |
                     +-----------+---------------------------+---------------------------+
                     | \\n       | Newline Character (ASCII) | Terminates a command or   |
                     |           |                           | inline comment.           |
                     +-----------+---------------------------+---------------------------+
                     | ``;``     | Semicolon                 | Explicit newline,         |
                     |           |                           | equivalent to a newline.  |
                     +-----------+---------------------------+---------------------------+
                     | ``\``     | Escape                    | Begins an escape          |
                     |           |                           | sequence, which can       |
                     |           |                           | represent newlines (\n),  |
                     |           |                           | and tabs (\t).            |
                     +-----------+---------------------------+---------------------------+
                     | ``.``     | Dot                       | Accesses library          |
                     |           |                           | functions and structure   |
                     |           |                           | attributes. (This is not  |
                     |           |                           | a decimal point.)         |
                     +-----------+---------------------------+---------------------------+
                     | ``_``     | Underscore                | When a command begins     |
                     |           |                           | with this operator, a     |
                     |           |                           | block of statements ends. |
                     +-----------+---------------------------+---------------------------+
                     | ``#``     | Hash                      | Start inline comment.     |
                     |           |                           | Everything to the right   |
                     |           |                           | is a comment.             |
                     +-----------+---------------------------+---------------------------+
                     | ``##``    | Double Hash               | Frames a multiple line    |
                     |           |                           | comment.                  |
                     +-----------+---------------------------+---------------------------+

                  .. rubric:: Grammar in EBNF
                     :name: grammar-in-ebnf

                  ::

                     Program := Header, Body
                     Header := {Include}, {(Macro | Struct)}
                     Body := {Func}
                     Macro := 'macro', Sp, Word, Lt | 'macro', {Statements}, '_macro', Lt
                     Struct := Stead, {Stine}, '_struct', Lt
                     Func := Fi, {Statement}, Re
                     Fi := 'func', Identifier, Lt
                     Re := ('return' | '_func'), {Arg}, Lt
                     Stead := 'struct' Identifier, Lt
                     Stine := Command, Identifier, Lt
                     Statement := Command, {Arg}, Lt
                     Command := {Sp}, Word, Sp
                     Arg := {(Number | Var | String | Identifier | Call | Word), Sp}
                     Call := ':', Word {'.', Word}
                     Var := (And, Word) | (Var '(', Var, ')') | (Var '(', Integer, ')') | Var, '.', Word
                     Identifier := '@', Words
                     Number := any number
                     Integer := any integer
                     Word := any set of non-white space characters
                     String := ' " ', (Word | Sp | Tab), ' " '
                     And := '&'
                     Sp := ' ', {' '}, Tab
                     Tab := a tab character
                     Lt := a newline char | ';' | '#'
                     Comment '#', {Word, Sp} | '##', {Word | Sp | Lt}, '##'

                  ::

                     Key:
                     := assignment, equivalence
                     | or
                     (group)
                     {repeated zero or more times}
                     [optional]
                     'string literal'
                     symbol
                     , symbol concatenation
                     ; symbol terminator
                     (*comment*)

                  .. rubric:: Compiling and Interpreting
                     :name: compiling-and-interpreting

                  bellbase makes use of a compiler and an interpreter to
                  run programs. Compiling happens at compile time. Then
                  interpreting happens at run time. All compiled
                  statements are processed outside of a function, like
                  includes, structs, and macros. All interpreted
                  statements are executed inside of a function.

                  **The compiler does the following:**

                  -  Uses a linker to read all included files into
                     memory and concatenates them together for
                     interpretation.
                  -  Processes all macros and performs replacements in
                     memory.
                  -  Analyzes all structs and generates the associated
                     data types for use in interpretation.
                  -  Analyzes all functions, storing labels, and binding
                     calls to their respective functions.
                  -  Parses the source code with lexical and syntactic
                     analysis.
                  -  Throws any relevant errors.

                  **The interpreter does the following:**

                  -  Executes compiled code starting at the main
                     function.
                  -  Executes commands in order, until the program
                     completes.
                  -  Throws an error if needed, and stops execution.
                  -  Outputs information for debugging.

                  .. rubric:: Variables
                     :name: variables

                  .. rubric:: Data Types
                     :name: data-types

                  bellbase stores data with variables. The following
                  types are usable:

                  .. table:: Types

                     +------------+---------------------------+---------------------------+
                     | Type       | Desc.                     | Range                     |
                     +------------+---------------------------+---------------------------+
                     | ``int``    | A four byte integer.      | -2,147,483,648 to         |
                     |            |                           | 2,147,483,647             |
                     +------------+---------------------------+---------------------------+
                     | ``float``  | A four byte value with a  | 3.4E +/- 38 (7 digits)    |
                     |            | decimal point.            |                           |
                     +------------+---------------------------+---------------------------+
                     | ``double`` | An eight byte value with  | 1.7E +/- 308 (15 digits)  |
                     |            | a decimal point.          |                           |
                     +------------+---------------------------+---------------------------+
                     | ``long``   | A type of eight bytes.    | -                         |
                     |            |                           | 9,223,372,036,854,775,808 |
                     |            |                           | to                        |
                     |            |                           | 9,223,372,036,854,775,807 |
                     +------------+---------------------------+---------------------------+
                     | ``char``   | A printable character, of | 0 to 255                  |
                     |            | one byte.                 |                           |
                     +------------+---------------------------+---------------------------+
                     | ``string`` | A printable string in     | none                      |
                     |            | quotes.                   |                           |
                     +------------+---------------------------+---------------------------+
                     | ``list``   | An array or list of items | none                      |
                     |            | in brackets. Items can be |                           |
                     |            | of any type.              |                           |
                     +------------+---------------------------+---------------------------+
                     | ``path``   | A path to a file.         | none                      |
                     +------------+---------------------------+---------------------------+
                     | ``func``   | A function, passed by     | none                      |
                     |            | reference.                |                           |
                     +------------+---------------------------+---------------------------+

                  A programmer can define their own types with
                  structures.

                  .. rubric:: Declaring Variables: The Refer Operator
                     ``&``
                     :name: declaring-variables-the-refer-operator

                  Each type is a command. These commands can take a name
                  and a value. The latter of which initializes the
                  variable. All variables are referred to with
                  ampersands. These are called refer operators, or
                  refers.

                  | 
                  | Examples:

                  ::

                     #use an identifier to create a var and a refer to refer to the var
                     int @i 20 
                     string @s "Hello"                   

                  ::

                     # &i is 20
                     # &s is "Hello"

                  A variable's type cannot change after declaration, and
                  two variables cannot have the same name. An
                  uninitialized variable is 0 by default, including
                  collections like strings, lists, and structures.

                  .. rubric:: Null Data
                     :name: null-data

                  0, the number, and null (no data here) are equivalent
                  in this language. A variable of any type can be set to
                  0.

                  When a collection is null, it cannot have indexes; a
                  null collection is distinct from an empty collection.
                  When a structure is null it cannot have attributes; a
                  null structure is distinct from a structure that has
                  null attributes.

                  .. rubric:: Assignment
                     :name: assignment

                  Assignment, or setting a variable to a value, can be
                  accomplished at initialization (shown above) or via
                  the set command. Variables can be assigned values of
                  their own type, but not values of a different type
                  without casting.

                  ::

                     set &i 21 
                     # &i is now 21

                  .. rubric:: Casting
                     :name: casting

                  Numbers can be cast to other numbers, but collections
                  cannot be cast to other collections.

                  Suppose a float is declared:

                  ::

                     float @f 0 

                  To cast it to an int, let the int command take the
                  variable ``&f``. In this example, an integer is
                  increased by the floor of f:

                  ::

                     int @i
                     give &i (:int &f)

                  | 
                  | Casting with collections gives an unexpected type
                    error.

                  .. rubric:: Constants
                     :name: constants

                  In this line, a variable is set to a constant.

                  ::

                     const &i #&i is now a constant

                  This variable cannot be modified after this point. It
                  will have the same value for the duration of its life,
                  and trying to modify it throws an error. If this
                  variable is a structure with attributes, the
                  attributes are also constants.

                  .. rubric:: Lists, Indexing, and Nesting
                     :name: lists-indexing-and-nesting

                  Lists are divided into items. Each item in a list has
                  an index. The leftmost index is 0. Each index refers
                  to a variable in the list.

                  ::

                     list &b [10 "Hello" 6.28]
                     # &b[0] is 10, &b[1] is "Hello" 

                  Lists can contain other lists to arbitrary depth.
                  Indexes can also be nested to arbitrary depth.

                  ::

                     list &b [10 [23 32] 34] # &b[1][1] is 32 

                  Syntactically, indexes are variables and should be
                  interpreted as such. Referring to an index that does
                  not exist gives a bad reference error.

                  .. rubric:: Strings and Escapes
                     :name: strings-and-escapes

                  Strings are interpreted literally, as text. A string
                  is framed by quotes and can include white space. A
                  string is always one argument, even one with spaces in
                  it.

                  For example, consider this line.

                  ::

                     out "Hello World &s" 

                  It outputs ``Hello World &s`` to the console. The
                  entire string, including spaces, is one argument,
                  output by the command.

                  .. rubric:: Escape Sequences
                     :name: escape-sequences

                  These are character codes for representing specific
                  characters inside a string, indicated by a backslash
                  and a letter.

                  .. table:: Escapes

                     ====== ===============
                     Escape Desc.
                     ``\n`` Newline
                     ``\r`` Carriage return
                     ``\t`` Tab
                     ``\"`` Quote
                     ``\#`` Hash
                     ``\\`` Backslash
                     ====== ===============

                  Example:

                  ::

                     out "Hello\nWorld" 

                  Output:

                  ::

                     Hello
                     World

                  .. rubric:: Character Access
                     :name: character-access

                  String characters can be accessed via the indexing
                  syntax

                  This example prints the first character of a string:

                  ::

                     func @main
                      string @s "dog"
                      out &s[0] #outputs d
                     return

                  .. rubric:: Identifiers: How to Use the Identifying
                     Operator ``@``
                     :name: identifiers-how-to-use-the-identifying-operator

                  These are used when naming a construct, like a
                  function, label, variable, or struct. This practice
                  enforces readability and prevents abuses of syntax. In
                  earlier versions, untyped words were used for naming,
                  but this was problematic.

                  Identifying a variable:

                  ::

                     int @i 10

                  Identifying a function:

                  ::

                     func @foo (:int @a) #a is an integer.

                  Identifying a struct:

                  ::

                     struct @tree

                  Identifying a label:

                  ::

                     label @foo

                  The identifying operator (``@``) is not part of a
                  name, it indicates a name.

                  .. rubric:: Labels and Conditionals
                     :name: labels-and-conditionals

                  Goto statements change the control flow of a program
                  by moving the program counter from one line to
                  another. In a program with no goto statements or
                  calls, lines are executed from the first to the last
                  in order, top to bottom. These programs cannot perform
                  logic, parse input, or make decisions. The program
                  counter needs to be able to jump in order for
                  computation to be possible.

                  Goto statements make the program counter jump. Labels
                  are locations to which the program counter jumps. In
                  combination, they can evaluate conditions and execute
                  loops. Finally, note that labels are stored at
                  compile-time, so a goto can accept a label that is
                  declared on a later line.

                  .. rubric:: Conditionals and Loops
                     :name: conditionals-and-loops

                  A conditional is a statement that can be true or false
                  if a condition is met. When a conditional is true, the
                  program counter goes to the label specified.
                  Otherwise, the program counter increments to the next
                  statement.

                  Loops begin with a label and end with a goto. They can
                  run until a condition is met, or they can run forever.
                  Count-controlled loops increment a number until it is
                  of a specific value. Sentinel-controlled loops run
                  until a condition is met.

                  .. rubric:: Commands and Examples
                     :name: commands-and-examples

                  -  See the "Conditionals and Loops" section of
                     Commands for information on commands that go to
                     labels.
                  -  For an example of conditionals with an infinite,
                     sentinel-controlled loop, see Truth Machine in
                     Program Examples.
                  -  For an example of conditionals with a
                     count-controlled loop, see FizzBuzz in Program
                     Examples.

                  .. rubric:: Structs: Defining a Data Type
                     :name: structs-defining-a-data-type

                  .. rubric:: What is a Structure?
                     :name: what-is-a-structure

                  Structures are data structures defined in source.

                  ::

                     struct @thing
                      int @i
                      int @j
                      int @k
                     _struct

                  | 
                  | Variables in structures, called attributes, are not
                    initialized. They are accessed and modified by
                    functions, such as in the example here:

                  ::

                     func @main
                      thing @s
                      set &s.k 10
                      out &s.k
                     return
                     #outputs 10

                  | 
                  | Structures can have attributes of their own type.
                    This is useful for defining data structures. This
                    example defines a binary tree.

                  ::

                     struct @binary_tree
                      node @root
                     _struct
                      
                     #node
                     struct @node
                      int @data
                      node @left   #child one
                      node @right  #child two 
                     _struct

                  .. rubric:: Initialization
                     :name: initialization

                  An uninitialized variable of a structure type has no
                  attributes at all, it is not a structure with null
                  attributes, but a variable with no data at all. To
                  initialize this variable, that is, give it data, a set
                  block or list is used:

                  | 

                  ::

                     struct @binary_tree
                      node @root
                     _struct
                      
                     #node
                     struct @node
                      int @data
                      node @left   #child one
                      node @right  #child two 
                     _struct

                  ::

                     func @main
                      set (:binary_tree @t) [0] #evaluates to &t [0] where &t is a tree with a null root
                      set &t.root
                       int 10
                       node &left  0 
                       node &right 0 
                      _set
                     return

                  .. rubric:: Notes
                     :name: notes

                  -  Note that referring to an attribute of a null
                     structure throws a bad reference error.
                  -  Note that structures cannot be defined within a
                     function.
                  -  Note that structure definitions cannot nest.

                  .. rubric:: Functions
                     :name: functions

                  All memory in this language is bound to functions (or
                  subroutines, if you prefer that term). Calls to
                  functions are stored in the function tree. The main
                  call is the root of this tree, and it branches each
                  time a call is made.

                  .. rubric:: The Basics: Functions and Calls
                     :name: the-basics-functions-and-calls

                  Functions let a programmer define their own commands
                  as subprograms, and they can be called to perform a
                  task. A function call executes the sub program defined
                  by a function. Calls cannot run include statements,
                  but they can take input, store information in memory,
                  and output to calling (parent) function calls. After
                  processing include statements, all Bellbase programs
                  call the main function implicitly. Every function
                  called from the main function is a child of the main
                  function call.

                  The ‘func’ command starts a function definition. It
                  takes a function name and input arguments for the
                  function. Functions end with a ‘return’ command, which
                  can output to the parent call.

                  When a function is called, execution stops for the
                  parent call, and resumes when the child call completes
                  execution. The program ends when the main call
                  completes or when a halt command executes.

                  .. rubric:: Specifying Function Input Types
                     :name: specifying-function-input-types

                  Sometimes a programmer needs to specify what type of
                  arguments their function can take:

                  .. table:: Typings

                     +---------------+-----------------------------------------------------+
                     | Example       | Desc.                                               |
                     +---------------+-----------------------------------------------------+
                     | ``@foo``      | foo is an identifier. Many commands take these.     |
                     +---------------+-----------------------------------------------------+
                     | ``:foo``      | foo is a call.                                      |
                     +---------------+-----------------------------------------------------+
                     | ``(:t @foo)`` | foo is a value the type specified; t is generic for |
                     |               | an int, float, double, long, char, string, list,    |
                     |               | path, or struct.                                    |
                     +---------------+-----------------------------------------------------+

                  .. rubric:: Function Calls as Arguments: The Call
                     Passing Operator ``:``
                     :name: function-calls-as-arguments-the-call-passing-operator

                  Function calls are first class in this language. They
                  can be assigned to a cell, passed to a function, or
                  returned from a function.

                  ::

                     foo :bar #passes what bar returns to foo.
                     foo (:bar @i 10 20) #bar can take arguments.

                  .. rubric:: Overloading
                     :name: overloading

                  A function is said to be overloaded when two function
                  definitions share the same name.

                  ::

                     func @foo (:string @a)
                      out &a
                      return

                  ::

                     func @foo (:int @a)
                      give &a 1
                      out &a
                      return

                  The function foo can output a string, or increment an
                  integer by one and output. Overloaded functions can
                  differ by the number of arguments they take and the
                  types of arguments they take. However functions cannot
                  share name, number of arguments, and types of
                  arguments. Here is an example of what not to do.

                  ::

                     func @foo
                      out "Hi"
                      return

                  ::

                     func @foo
                      out "Bye"
                      return

                  This overloaded function is ambiguous and produces a
                  collision. If foo were called, the output of that call
                  is indeterminate. The two definitions of foo collide.

                  .. rubric:: Returning
                     :name: returning

                  A return outputs from a function call to its parent.
                  In the case where a call is an argument of a call or
                  command, the argument is evaluated first. Let ``&d``
                  be 2 in this example.

                  ::

                     bneq (:give 3 &d) 0 # -> bneq 5 0

                  The arrow is not an operation, it demonstrates
                  evaluation.

                  .. rubric:: Referring to Functions
                     :name: referring-to-functions

                  Recall the table of data types. Functions and calls
                  are data types, and they can be referenced with the
                  refer operator. A function reference takes an
                  identifier, and a function (header and body). It is a
                  function definition. These are in a scope such that
                  all functions can reference other functions.

                  A command called call can run a call passed by
                  reference. ``(:foo 1 2)`` is equivalent to:

                  ::

                     call &foo [1 2]

                  .. rubric:: Functions as Attributes of Structures
                     :name: functions-as-attributes-of-structures

                  A structure can reference a function as an attribute,
                  shown here:

                  ::

                     struct @foo
                      func &bar
                     _struct

                  Such a structure can accept and run any function it
                  references, in general this is useful for binding data
                  to a function call.

                  .. rubric:: Macros
                     :name: macros

                  Macros are substitutions performed by the compiler
                  before runtime.

                  .. rubric:: Use as Constants
                     :name: use-as-constants

                  Consider this example with no macros:

                  ::

                     func @main
                      list @b [9 8 7] 
                      give &b[0] 10
                      give &b[1] 10 
                      give &b[2] 10 
                     return

                  | 
                  | To swap 10 for 11, three lines need to be changed.

                  Now consider this example with macros:

                  ::

                     macro !foo 11
                     func @main
                      list @b [9 8 7] 
                      give &b[0] !foo
                      give &b[1] !foo 
                      give &b[2] !foo 
                     return

                  Only one line needs to be changed. It's nicer.

                  .. rubric:: Blocks
                     :name: blocks-1

                  Macros can be multiple lines long, which is great for
                  consolidating repeated code and simplifying source.

                  .. rubric:: Files
                     :name: files

                  Note this excerpt from Commands:

                  ::

                     out
                          This prints the value given. Standard output is default, 
                          but the second argument specifies a file for writing.  
                          The file content is not overwritten. Data is appended.
                          Args: VALUE, [PATH]
                     read
                         Loads file content into memory; takes a file path and returns a string.
                         Args: PATH
                     ovwr
                         Overwrite file (arg2), with content (arg1)
                         Args: STRING, PATH
                     make
                         Make a file (0) or directory (1) at the specified path.
                         Args: INTEGER, PATH
                     del
                         Delete file or directory (recursively) at path.
                         Args: PATH

                  There actually is not much to say about files.
                  Directories are folders, which contain files, which
                  contain data that can be read into a program,
                  overwritten, or given new data to add to the file
                  somewhere.

                  .. rubric:: Errors
                     :name: errors

                  .. rubric:: Error Codes
                     :name: error-codes

                  ::

                     Syntax Error [Command Doc] [Int Range] ::: (1)
                     File Not Found ::::::::::::::::::::::::::: (2)
                     End Of File :::::::::::::::::::::::::::::: (3)
                     Undefined Variable ::::::::::::::::::::::: (5)
                     Undefined Function ::::::::::::::::::::::: (4)
                     Undefined Label :::::::::::::::::::::::::: (5)
                     Conflicting Identifiers :::::::::::::::::: (6)
                     Conflicting Function Definitions ::::::::: (7)   
                     Conflicting Labels ::::::::::::::::::::::: (8)
                     Unexpected Argument Type ::::::::::::::::: (9)
                     More Arguments Expected ::::::::::::::::: (10)
                     Missing Main Function ::::::::::::::::::: (11)
                     Unmatched Parenthesis ::::::::::::::::::: (12)
                     Unmatched Bracket ::::::::::::::::::::::: (13)
                     Compiler Error; Check Statements :::::::: (14)
                     Cannot Compile in Function :::::::::::::: (15) 
                     Undefined Macro ::::::::::::::::::::::::: (16) 
                     Runtime Error ::::::::::::::::::::::::::: (17)
                     Stack Overflow :::::::::::::::::::::::::: (18)
                     Out of Memory ::::::::::::::::::::::::::: (19)
                     Bad Argument :::::::::::::::::::::::::::: (20)
                     Bad Reference ::::::::::::::::::::::::::: (21)
                     Cannot Modify Constant :::::::::::::::::: (22)
                     Cannot Nest Blocks :::::::::::::::::::::: (23)
                     Error ::::::::::::::::::::::::::::::::::: (24)

                  To clarify the use of adjectives: **Undefined** means
                  that the error is thrown by an argument that requires
                  a definition in source. **Conflict** occurs when the
                  next command to execute cannot be determined because
                  of a shared name or header. **Bad** means that the
                  erroneous code is incomputable, like a negative wait
                  time, or a reference to data that is not there.

                  Whenever possible, an error should describe the
                  function and instruction at which it occurred. A trace
                  of calls should be printed whenever an error is
                  thrown; each call should list all of its arguments on
                  one line if applicable.

                  Whenever it is applicable, a doc string should be
                  printed describing the syntax of the erroneous
                  command. If this command is defined by the user, the
                  function source will be printed

                  .. rubric:: Example of Call Trace
                     :name: example-of-call-trace

                  ::

                     foo 213
                     bar
                     main

                  .. rubric:: Example of Command Doc String
                     :name: example-of-command-doc-string

                  ::

                     bell 
                          Don’t you know? A bell goes ding! 
                          It makes sound!
                          Args: [HERTZ, [DURATION IN MILLIS]]

                  .. rubric:: Example of Function Print
                     :name: example-of-function-print

                  ::

                     func @cat
                        out "Feed the cat\n"
                        out (:input 2)
                        doc "This function asks for input and prints that."
                     return

                  .. rubric:: Writing a Doc String
                     :name: writing-a-doc-string

                  The ``doc`` command can accept a string or a block of
                  text. A one line doc string is shown above, but a
                  block of text does not require quotes at all. All text
                  in this block is literal. The interpreter skips this
                  block entirely.

                  ::

                     doc
                     Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
                     Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                     Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. 
                     Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                     _doc 

                  | 

                  ::

                     func @main
                      out "Hello World" 
                      return 

                  .. rubric:: Throwing, Catching, and Handling Errors
                     :name: throwing-catching-and-handling-errors

                  Errors can be caught and handled inside handle blocks.
                  A handle block catches an error and executes a goto
                  statement. Errors can be thrown by passing an error
                  code to the error command. Like all block statements,
                  handles cannot nest. Here is an excerpt from the
                  Commands section:

                  ::

                     handle 
                          Go to the label if any of the listed errors occurs in a handle block.
                          Args: LABEL, LIST OF ERRCODES
                     _handle
                          Ends the handle block above.
                     error 
                          Throws the error given.
                          Args: INTEGER.

                  .. rubric:: Commands
                     :name: commands

                  (Note that arguments listed in [brackets] are
                  optional)

                  .. rubric:: Functions
                     :name: functions-1

                  ::

                     func
                          Defines a function with or without arguments
                          Args: IDENTIFIER, [FUNCTION ARGUMENTS]
                     func
                          Accepts a reference to a function, typically as a struct attribute.
                          Args: FUNCTION REFERENCE (A VALUE)
                     return
                          Ends a function and returns arguments given.
                          If there is nothing to return, 0 is returned.
                          Args: [VALUE]
                     _func
                          Equivalent to a return command. 
                          Args: [VALUE]
                     call
                          Runs a call when given a function reference.
                          Args: FUNCTION REFERENCE [LIST OF ARGUMENTS]
                     doc
                         This command defines a doc string for a function.
                         Doc strings explains what a function does and how 
                         it should be used.
                         The doc string starts on the next line and
                         execution skips to the end of the doc string.
                     _doc
                         End doc string; resume execution.

                  .. rubric:: Input and Output
                     :name: input-and-output

                  ::

                     out
                          This prints the value given. Standard output is default, 
                          but the second argument specifies a file for writing.  
                          The file content is not overwritten. Data is appended.
                          Args: VALUE, [PATH]
                     input
                          Takes input of the data type given 
                          (with the exclusion of lists and structs).
                          Args: STRING
                     read
                         Loads file into memory; takes a file path and returns a string.
                         Args: PATH
                     ovwr
                         Overwrite file (arg2), with content (arg1)
                         Args: STRING, PATH
                     bell 
                          Don’t you know? A bell goes ding! 
                          It makes sound!
                          Args: [HERTZ, [DURATION IN MILLIS

                  .. rubric:: Conditionals and Loops
                     :name: conditionals-and-loops-1

                  ::

                     label
                          A label to go to. These are not global, 
                          instead they are defined locally in a function. 
                          Args: IDENTIFIER
                     beq
                          Branch to LABEL if args are equal.
                          Args: NUMBER, NUMBER, LABEL  
                     bneq 
                          Branch to LABEL if args are not equal.
                          Args: NUMBER, NUMBER, LABEL 
                     bgr 
                          Branch to LABEL 
                          if arg1 is greater than arg2.
                          Args: NUMBER, NUMBER, LABEL    
                     bleq 
                          Branch to LABEL 
                          if arg1 is less than or equal to arg2.
                          Args: NUMBER, NUMBER, LABEL   
                     goto
                          Go to label specified
                          Args: LABEL

                  .. rubric:: Data
                     :name: data

                  ::

                     var 
                          Initializes a variable of the given type. 
                          Note that var is a genericized placeholder for a data type.
                          Pass it a value to initialize the variable.
                          Args: IDENTIFIER, [VALUE]   
                     var
                          To cast, pass a variable.
                          Args: VAR
                     set
                          Set variable to value.
                          Args: VAR, VALUE
                     set
                          Takes a variable that is a structure, 
                          and sets attributes in a list.
                          Args: VAR, LIST
                     set
                          Takes a variable that is a structure, 
                          and sets attributes in a block.
                          Args: VAR
                     _set
                          End set block.
                     const
                          The specified variable is now a constant.
                     millis 
                          Get the time since midnight of January 1, 1970, 
                          in milliseconds. Returns a long.

                  .. rubric:: Numeric Modifiers
                     :name: numeric-modifiers

                  ::

                     give
                          The first argument is set to the sum of itself and the second argument.
                          Args: VAR, NUMBER
                     take
                          The first argument is set to the difference of itself and the second argument.
                          Args: VAR, NUMBER

                  .. rubric:: Error Handling
                     :name: error-handling

                  ::

                     handle 
                          Go to the label if any of the listed errors occurs in a handle block.
                          Args: LABEL, LIST OF ERRCODES
                     _handle
                          Ends the handle block above.
                     error 
                          Throws the error given.
                          Args: INTEGER.

                  .. rubric:: File Management
                     :name: file-management

                  For File I/O see Input and Output

                  ::

                     make
                         Make a file (0) or directory (1) at the specified path.
                         Args: INTEGER, PATH
                     del
                         Delete file or directory (recursively) at path.
                         Args: PATH

                  .. rubric:: Program Interrupters (Excluding input)
                     :name: program-interrupters-excluding-input

                  ::

                     wait
                          Wait for a number of milliseconds 
                          (1000 if not specified).
                          Args: [TIME TO WAIT IN MILLIS]
                     halt   
                          End program.

                  .. rubric:: Compiled
                     :name: compiled

                  ::

                     struct 
                          Defines a data type as a block of variables.
                          Args: IDENTIFIER
                     _struct 
                          Ends a struct.
                     include
                          Include contents of specified file.
                          or directory
                          Args: PATH
                     macro
                          These are substitutions handled by the linker.
                          Argument one is the macro name
                          which always start with a bang (!).
                          !arg1 is replaced with arg2 at all points in source.
                          Args: MACRO_NAME, REPLACEMENT
                     _macro
                          If the second arg of a macro is a semi-colon, the macro can continue over multiple lines. 
                          This command ends the macro.
                     impl 
                          Short for implements, this is a command designed for interpreter extensibility.
                          It takes a path to a .bbim file in the extensions directory. 
                          This enables the interpreter to interpret commands defined in .bbim files.

                  .. rubric:: Using the Interpreter
                     :name: using-the-interpreter

                  The interpreter runs in a shell and takes command line
                  arguments:

                  ::

                     bbe file_to_run.bbe inputs_for_main_func -flag

                  -  ``inputs_for_main_func`` is a set of arguments for
                     the main function, separated by spaces.
                  -  The ``-flag`` sets the interpreter to mute, debug,
                     or both.

                  .. rubric:: Flagging
                     :name: flagging

                  The flag can be in four states

                  ::

                      -m mute the bell
                      -d debugger on
                     -dm mute the bell and debugger on
                     -md mute the bell and debugger on

                  .. rubric:: Muting
                     :name: muting

                  When mute, the bell should not make sound and it
                  should not output text. It is a no-op.

                  .. rubric:: The Debugger
                     :name: the-debugger

                  Every Bellbase interpreter should have a debugger that
                  prints the following at each step:

                  -  The current function call, with arguments.
                  -  The current instruction in full.
                  -  Value stored at the last variable accessed.
                  -  Any program output at that step.

                  **Example Debug Output:**

                  ::

                     Current Function: messages
                     Current Instruction: out "Here are your messages."
                     Last Variable Modified: &v
                     Variable State: 9
                     Output:
                     Here are your messages.

                  .. rubric:: Inputs
                     :name: inputs

                  When a program is waiting for user input it should
                  output a right angle bracket and a space:

                  ::

                     > Lorem Ipsum

                  .. rubric:: The Linker: Include Commands
                     :name: the-linker-include-commands

                  .. rubric:: How to use Includes
                     :name: how-to-use-includes

                  The linker formats source code so that it can run
                  appropriately. All leading whitespace before an
                  instruction is removed. Additionally, all include
                  commands are processed. The contents of each included
                  file are compiled for use.

                  Note that source files are run from a run directory.
                  Here are examples of include commands:

                  ::

                     include run\foo\bar\hello.bbe
                     include ->dog\cat\*

                  As explained in Useful Operations, the right arrow is
                  substituted with the path from *run* to the current
                  file, and star includes the entire contents of a
                  directory.

                  .. rubric:: Using a Library
                     :name: using-a-library

                  Libraries are directories that contain source files.
                  These should be stored in a directory called *lib*.
                  This directory should be stored in the same location
                  as *run*.

                  Example:

                  ::

                     include lib\Math.bbe

                  .. rubric:: On Cyclic File References
                     :name: on-cyclic-file-references

                  TL;DR detecting these is an operationally expensive
                  way to do a whole lot of nothing. If a programmer has
                  one of these by mistake, they probably also have an
                  infinite recursion anyway, and they will get a stack
                  trace that alerts them to the bug.

                  Consider this example:

                  #. File A.bbe has the statement ``include B.bbe``
                  #. File B.bbe has the statement ``include A.bbe``

                  These are generally difficult to handle efficiently.
                  While they can be detected by generating a graph of
                  linked files, and checking for a Hamiltonian cycle.
                  This would be done in polynomial time and slow the
                  interpreter down. Even internationally recognized,
                  professionally implemented languages, like C and
                  Python, are often not implemented in ways that
                  explicitly deal with cyclic references. Explicit
                  handling of cyclic include references is, in general,
                  too costly to bother with.

                  The more common, and simpler case, is infinite
                  recursions on the call stack. These are easily
                  demonstrated via tracing and printing the call stack
                  in linear time. Such a case is relevant to cyclic file
                  references because files linked in a cycle are likely
                  to make function calls that produce an infinite
                  recursion. Ie, file A calls a function in file B. Then
                  file B calls a function in file A. In general, if
                  there is an unintentional cyclic file reference, it is
                  probably going to be discovered by means of an
                  infinite recursion anyway, so having an explicit way
                  to detect cycling files is not necessary.

                  .. rubric:: Libraries
                     :name: libraries

                  The following libraries are included in a Bellbase
                  interpreter.

                  .. rubric:: Math
                     :name: math

                  **Ops**

                  This library has functions that operate on two
                  numbers. Each returns an integer.

                  ::

                     add
                        adds stuff
                     sub
                        subtracts stuff
                     mul
                        multiplies stuff
                     div
                        integer division
                     mod
                        modulo 
                     pow
                        raise arg1 to arg2
                     root
                        takes the arg2 root of arg1
                     random
                        returns a random value between 0 and 1
                     randint 
                        returns a random integer between arg1 and arg2 inclusive.
                     floor
                        returns the floor of a float or double as an int.
                     ceiling
                        returns the ceiling of a float or double as an int.
                     abs
                        returns the absolute value of a number.
                     sin
                        returns the sine of a number.
                     cos
                        returns the cosine of a number.
                     tan
                        returns the tangent of a number.

                  **Consts**

                  ::

                     pi 
                        returns pi as a double 
                     e
                        returns e as a double 
                     phi
                        returns phi as a double

                  .. rubric:: Data
                     :name: data-1

                  **Collect**

                  Operations on collections.

                  ::

                     size
                        Get the number of items in a collection.
                        Args: COLLECTION
                        Ret:  INTEGER
                     count
                        Counts the occurrences of a value.
                        Args: COLLECTION, VALUE 
                        Ret:  INTEGER
                     cat
                        Concatenates strings into one string. 
                        Args: STRING, STRING
                        Ret:  STRING
                     cat
                        Concatenates lists into one list. 
                        Args: list, list
                        Ret:  list
                     make_empty_list
                        Makes an empty list (of null data) of a given size.
                        Args: INTEGER
                        Ret:  list
                        Err: Bad Argument if Negative integer
                     append 
                       To use with a list. 
                       The list size grows by 1 and the item becomes the last index in the list.
                       Args: list, VALUE
                     remove 
                       Remove the index given from the list.
                       Args: list, VAR
                       Err: If the index is not found, that’s an undefined var.
                     insert
                       Insert item at index of list.
                       Args: list, INDEX, VALUE
                       Err: Not a list or index

                  **Consts**

                  ::

                     maxInt
                       returns maximum integer value
                     minInt
                       returns minimum integer value
                     maxLong
                       returns maximum long value
                     minLong
                       returns minimum long value
                     maxFloat
                       returns maximum float value
                     minFloat
                       returns minimum float value
                     maxDouble
                       returns maximum double value
                     minDouble
                       returns minimum double value

                  **Compare**

                  This is a library for comparing collections.
                  Collections are converted to integers and evaluated.

                  How collections are compared:

                  -  Strings are a sum of characters.
                  -  Lists are a sum of items.
                  -  Structs are a sum of attributes.
                  -  Functions are always 0, as they are not generally
                     comparable.

                  Two sums A and B, are calculated then B - A is
                  returned. Equal values return 0. B > A returns a
                  positive value. A < B returns a negative value.

                  ::

                     compare
                       Compares two strings.
                     compare
                       Compare two lists recursively. 
                     compare
                       Compare two structs by attributes recursively. 

                  The convention for naming library files is to write
                  the name of the library and bbe. The Collect file is
                  **Collect.bbe** in the directory **lib\Data**

                  .. rubric:: Proof of Turing Completeness
                     :name: proof-of-turing-completeness

                  .. rubric:: Proof by Translation to bf
                     :name: proof-by-translation-to-bf

                  It is trivial to define a function that can simulate a
                  bf interpreter. Bf stores memory as cells on a tape.
                  Cells are modified by a movable pointer, exactly like
                  a Turing machine. A list of characters is sufficient
                  to implement the tape.

                  ::

                     func @bf
                      list @tape (:make_empty_list 30000)
                      int @pointer 0 #points to a char

                      ##
                      translated bf goes here
                      ##

                     return

                  .. table:: Translation Table

                     ===== =============================================================
                     bf    Bellbase
                     ``>`` ``give &pointer 1;``
                     ``<`` ``take &pointer 1;``
                     ``+`` ``give &tape[&pointer] 1;``
                     ``-`` ``give &tape[&pointer] -1;``
                     ``.`` ``out &tape[&pointer];``
                     ``,`` ``input &tape[&pointer] "char";``
                     ``[`` ``beq &tape[&pointer] 0 @closeBracket; label @openBracket;``
                     ``]`` ``bneq &tape[&pointer] 0 @openBracket; label @closeBracket;``
                     ===== =============================================================

                  (The semicolon is an explicit newline.)

                  Given bf is Turing complete, and bellbase can simulate
                  a bf interpreter. bellbase must also be Turing
                  complete. QED

                  .. rubric:: Syntax Highlighting
                     :name: syntax-highlighting

                  Syntax highlighting is a practice to improve
                  readability by coloring tokens. Keep in mind that a
                  readable source code is best achieved in a language
                  with appropriate syntax. Readable code does not
                  require highlights at all.

                  As a general rule of thumb: tokens that require
                  specialized parsers have hue, and tokens are otherwise
                  black or white. The color scheme below is not a
                  mandate, but an attempt.

                  .. rubric:: Colors
                     :name: colors

                  -  ERRORS range from red to orange; if preferred,
                     black or white is also acceptable.
                  -  IDENTIFIERS range from red to yellow
                  -  VARIABLES and NUMBERS range from yellow to blue
                  -  MACROS range from green to blue
                  -  STRINGS and DOC STRINGS range from blue to purple.
                  -  CALLS and COMMANDS range from purple to pink.
                  -  COMMENTS are gray.
                  -  PARENTHESES, BRACKETS, SEMI-COLONS, DOTS, LABELS,
                     and PATHS are black or white.
                  -  BLACK is hex code #031930
                  -  WHITE is hex code #fce6cf

                  This scheme should be modified as needed for
                  colorblindness, theme, mode, or whim. Two colorblind
                  adapted palettes are available. Note that a dark
                  reader may interfere with the rendering of palettes.
                  Also note that as implied in the palettes, the
                  operators are highlighted according to token color.

                  .. rubric:: General Palettes
                     :name: general-palettes

                  Lakeside palette:

                  ::

                     error
                     @identifier
                     number
                     &variable
                     !macro
                     "string"
                     command
                     :call
                     #comment
                     ()[];.
                     label
                     path
                     error

                  Forest palette:

                  ::

                     error
                     @identifier
                     number
                     &variable
                     !macro
                     "string"
                     command
                     :call
                     #comment
                     ()[];.
                     label
                     path
                     error

                  Plateau palette (This is used in documentation for
                  light and dark reading.)

                  ::

                     error
                     @identifier
                     number
                     &variable
                     !macro
                     "string"
                     command
                     :call
                     #comment
                     ()[];.
                     label
                     path
                     error

                  .. rubric:: Adapted Palettes
                     :name: adapted-palettes

                  IBM Design Library:

                  ::

                     error
                     @identifier
                     number
                     &variable
                     !macro
                     "string"
                     command
                     :call
                     #comment
                     ()[];.
                     label
                     path
                     error

                  Wong, Points of View: Color Blindness. Nature Methods:

                  ::

                     error
                     @identifier
                     number
                     &variable
                     !macro
                     "string"
                     command
                     :call
                     #comment
                     ()[];.
                     label
                     path
                     error

                  .. rubric:: Interpreter Extensibility
                     :name: interpreter-extensibility

                  The interpreter should be implemented such that it can
                  accept command modules, such as ``.bbim`` files that
                  can define additional commands for the interpreter.
                  These files would be located in a directory in **bbe**
                  called **ext**. These extended commands would be
                  implemented in source via a compiler command.
                  ``impl``. These ``.bbim`` are called extensions.

                  .. rubric:: Defining Commands
                     :name: defining-commands

                  Files would describe commands with command blocks. The
                  command takes an identifier as a name such as
                  ``comm @foo``. The body of the command would run a
                  ``run`` command that one, takes a path to a file that
                  is written in the same language as the bellbase
                  interpreter, such that it can be run via the language
                  that implements bellbase; and two, takes a reference
                  (variable) that describes a function in the file
                  described by argument one.

                  The file described by the run command (let's call it
                  A) would be a file that includes necessary resources,
                  and wraps the code that describes the extended command
                  in a function. The ``.bbim`` file would be interpreted
                  such that when the commands defined in the ``.bbim``
                  are executed by the bellbase interpreter, the relevant
                  function in file A is run for each command.

                  Here is an example:

                  ::

                     comm @foo
                      run path_to_A &function_in_A
                     _comm

                  .. rubric:: Defining Errors
                     :name: defining-errors

                  To throw an error, simply have the run command return
                  the error code needed. 0 indicates that there is no
                  error. Codes 1 to 24 are error codes. 25 and above are
                  equivalent to 24. Negative values are interpreted as
                  absolute values, such that the positive error code is
                  returned.

                  .. rubric:: Test Cases
                     :name: test-cases

                  .. rubric:: Parser Tests
                     :name: parser-tests

                  -  Test each type of comment.
                  -  Test strings and docs strings.
                  -  Test for parenthesis and brackets
                  -  Test each operation.

                  .. rubric:: Command Tests
                     :name: command-tests

                  Note that each command should be tested with no
                  arguments, expected arguments, and unexpected
                  arguments.

                  .. rubric:: Error Tests
                     :name: error-tests

                  Each error should be tested.

                  .. rubric:: Library Tests
                     :name: library-tests

                  Each function in the library described should be
                  tested.

                  .. rubric:: Function Tests
                     :name: function-tests

                  -  One (non-main) function, one call, no arguments.
                     (Simplest Case)
                  -  One (non-main) function, one call, with value
                     arguments.
                  -  One (non-main) function, one call, with variable
                     arguments.
                  -  One (non-main) function, one call, with functions
                     as arguments.
                  -  One (non-main) function, one call, with mixed type
                     arguments.
                  -  One (non-main) function, one call, with unexpected
                     arguments.
                  -  One overloaded (non-main) function, one call, with
                     arguments.
                  -  One overloaded (non-main) function, multiple calls,
                     with arguments.
                  -  One overloaded (non-main) function, multiple calls,
                     with arguments, such that each call runs the same
                     subroutine with different inputs.

                  .. rubric:: Compiler Tests
                     :name: compiler-tests

                  -  Macro definition test.
                  -  Structure definition and use test.
                  -  Include one file in same directory.
                  -  Include one file in another directory.
                  -  Include file in subdirectory.
                  -  Include multiple files from various directories.
                  -  Include entire directory.
                  -  Include files in file to be included (accomplished
                     via the right arrow >).
                  -  Circular include reference.

                  .. rubric:: Index
                     :name: index

                  Much of the stuff here is explained in the docs or
                  rigorously defined elsewhere. This is not a textbook
                  and the definitions here are for those interested in
                  getting to the point.

                  .. rubric:: Algorithm
                     :name: algorithm

                  A procedure to do something or make a decision.

                  .. rubric:: ASCII Table
                     :name: ascii-table

                  A table in which textual characters are assigned to a
                  number. It was specifically designed for teleprinters
                  in the 1960s. A teleprinter is essentially a
                  typewriter that can be operated remotely. So, the
                  ASCII table features a lot of specific control signals
                  for operating the recipient's teleprinter. (7 rings a
                  bell, which is fun.) The ASCII table is essentially
                  the ancestor of all text encodings. Unless you are
                  using some kind of esoteric keyboard, the computer you
                  are using supports ASCII (including all of those old
                  teleprinter signals).

                  .. rubric:: Assignment
                     :name: assignment-1

                  Sets a variable to a value. If x is assigned 5 , then
                  x is now 5.

                  .. rubric:: Arguments
                     :name: arguments

                  These are not the emotional kind, or the kind of an
                  interlocutor. They are inputs for a command or
                  function.

                  .. rubric:: Array
                     :name: array

                  This is an ordered grouping of items. A list of stuff,
                  usually contiguous in memory. lists are arrays.

                  .. rubric:: Bell
                     :name: bell

                  This goes ding or beep. If you find yourself running a
                  program for hours, you can use these to alert you to
                  the program’s status while you are doing laundry.

                  If you prefer to run such a program while you sleep,
                  you can mute the bell. Just know that if you ignore
                  the computer for too long, it may crash out of spite,
                  and you will wake up to a friendly error message, and
                  you have to plan your evening around the needs of an
                  old computer, and you will question your life choices.

                  .. rubric:: Bf
                     :name: bf

                  A polite name for a language created by Urban Müller
                  in 1993. This language is designed to be the simplest
                  language possible, such that it has the smallest
                  compiler possible. It runs a Turing machine on a tape
                  of bytes and is proven to be Turing complete.

                  .. rubric:: Bit
                     :name: bit

                  The fundamental unit of information. A bit can be in
                  one of two states. You can think of it as a lightbulb.
                  A bit can be on or off, 0 or 1, true or false. A
                  contiguous set of bits is a word. A word of 2 bits has
                  four states. 3 bits have 8 states. One more bit
                  increases the number of states to the next power of
                  two.

                  .. rubric:: Bug
                     :name: bug

                  This is the chaotic code that broke your metaphoric
                  vase. You probably wrote it to do something, but you
                  made a mistake and now it does something else. On the
                  origin of the term, I offer this quote from the
                  biography of Rear Admiral Grace Murray Hopper:

                  "In 1946, when Hopper was released from active duty,
                  she joined the Harvard Faculty at the Computation
                  Laboratory where she continued her work on the Mark II
                  and Mark III. She traced an error in the Mark II to a
                  moth trapped in a relay, coining the term *bug*. This
                  bug was carefully removed and taped to the log book.
                  [Needless cruelty!] Stemming from the first bug, today
                  we call errors or glitch's in a program a *bug*."

                  One day in 1946 they found a literal bug inside some
                  very large, punch-card monstrosity of a machine. The
                  bug crawled in looking for warmth and a cozy shelter,
                  which is understandable. The bug was a bug, and it
                  could not comprehend the consequences of its actions.
                  It was making the computer do strange things. The
                  computer needed debugging, hence the origin of a new
                  term in the field. Hopefully, the bug was freed from
                  its tape prison to go about its bug life
                  uninterrupted.

                  .. rubric:: Byte
                     :name: byte

                  8 bits. Range of 0 to 255 (unsigned).

                  .. rubric:: Call
                     :name: call

                  This runs a function with inputs. These can have
                  parents and children. A parent call calls a child
                  call.

                  .. rubric:: Child
                     :name: child

                  Opposite of a parent. This call finishes execution
                  within parent scope.

                  .. rubric:: Command
                     :name: command

                  This is what you use to tell the computer to do a
                  thing.

                  .. rubric:: Comment
                     :name: comment

                  This is for people to read; it clarifies. The
                  interpreter cannot read these. As a rule, it is better
                  to explain why the code is written, not what it does,
                  when writing a comment.

                  .. rubric:: Compiler
                     :name: compiler

                  In computation, a compiler is a program that reads
                  source code and converts it into a form that can be
                  interpreted.

                  .. rubric:: Console
                     :name: console

                  This runs programs, takes input, and displays output.

                  .. rubric:: Constant
                     :name: constant

                  Data that cannot change state over time.

                  .. rubric:: Directory
                     :name: directory

                  A folder. It stores files.

                  .. rubric:: EBNF
                     :name: ebnf

                  This is Extended Backus-Naur Form. It is a meta-syntax
                  that describes the syntax of programming languages.

                  .. rubric:: Error
                     :name: error

                  Errors are the seatbelt that keeps your computer safe.
                  In this analogy, your program is a car and your
                  computer is the driver. Errors protect your computer
                  when your program does something that is unexpected.
                  Errors are distinguished by error codes.

                  .. rubric:: Esolang
                     :name: esolang

                  An esolang is an esoteric programming language. These
                  are usually designed by hobbyists to experiment with
                  concepts in programming and computation. Bellbase is
                  the least esoteric programming language in the history
                  of the esolangs wiki, and it is documented there out
                  of convenience. If that upsets you, perhaps you should
                  consider if being upset over such trivial things is
                  contributing positively to your life.

                  .. rubric:: File
                     :name: file

                  A happy little home for data.

                  .. rubric:: First Class
                     :name: first-class

                  Something is considered first class when it has the
                  following properties:

                  -  It can be assigned or stored in program memory
                     (RAM).
                  -  It can be passed to a function.
                  -  It can be returned from a function.

                  If these three criteria are not satisfied, the
                  construct is second-class.

                  .. rubric:: Function
                     :name: function

                  A program that is run by another program. A
                  subprogram. Takes input and returns output. The
                  function is defined as source code.

                  .. rubric:: Heap
                     :name: heap

                  This is a data structure that behaves like a large
                  pile of legos. You can use the legos to build houses
                  and spaceships and whatever else you like. (Just make
                  sure they go back in the box when you are done.) In
                  this language, the legos are variables, and the return
                  command cleans everything up.

                  .. rubric:: Initialization
                     :name: initialization-1

                  Uninitialized variables are null. The first time a
                  variable is assigned data, the variable undergoes
                  initialization.

                  .. rubric:: Input
                     :name: input

                  Data to be processed by a program.

                  .. rubric:: Interpreter
                     :name: interpreter

                  Interprets and executes source code line by line.

                  .. rubric:: Library
                     :name: library

                  A library is a set of files that contain useful
                  functions for programmers.

                  .. rubric:: Nesting
                     :name: nesting

                  Putting a thing inside another thing. It has nothing
                  to do with the 2011 movie *Inception*.

                  .. rubric:: Null
                     :name: null

                  This means "no data here". 0 is equivalent to null in
                  ASCII.

                  .. rubric:: Output
                     :name: output

                  Data generated by a program.

                  .. rubric:: Overloading
                     :name: overloading-1

                  A function is said to be overloaded when there are two
                  or more function definitions of the same name, but
                  differing arguments. The number of arguments may be
                  different, their typing may be different, or the
                  number and typing of the arguments may vary between
                  definitions.

                  .. rubric:: Parent
                     :name: parent

                  Calls the current call, when the current call is
                  finished execution returns to the parent.

                  .. rubric:: Program
                     :name: program

                  A to-do list for a computer. Completing the list is
                  called running or execution.

                  .. rubric:: Program Counter
                     :name: program-counter

                  This keeps track of what to do next. It will keep
                  incrementing after each statement, until the program
                  ends.

                  .. rubric:: Source Code
                     :name: source-code

                  This is what programs are written in.

                  .. rubric:: Stack
                     :name: stack

                  Think of a stack of pancakes, which is what I call the
                  yummy, pan-fried, tasties, though you might call them
                  flapjacks or hot cakes. Pancakes get on the stack from
                  the top, and the ones at the bottom get eaten last.

                  Sadly, function calls are not pancakes, the last call
                  on the stack creates the next call to go on the stack.

                  .. rubric:: Stack Overflow
                     :name: stack-overflow

                  Have you ever tried to make an endless stack of
                  pancakes? You use up all the batter and the stack
                  topples over. This error is thrown before toppling
                  happens. It stops someone from creating a stack with
                  an irresponsible amount of pancakes.

                  .. rubric:: Syntax
                     :name: syntax-1

                  This tells you how to read and write stuff in a
                  language.

                  .. rubric:: Token
                     :name: token

                  A token is the shortest portion of source an
                  interpreter can understand.

                  .. rubric:: Turing Complete
                     :name: turing-complete

                  Something that is Turing complete is capable of doing
                  any solvable math problem or deciding any decidable
                  problem. It can run any algorithm that is runnable.
                  Anything Turing complete can simulate anything else
                  that is Turing complete.

                  .. rubric:: Turing Machine
                     :name: turing-machine

                  A theoretical device that can be programmed to read
                  and write on an endless tape. The tape is divided into
                  cells that can store one bit. The machine is capable
                  of solving any solvable problem and is foundational in
                  computing. It was invented by Alan Turing.

                  .. rubric:: Variable
                     :name: variable

                  Data that can change state over time.

                  .. rubric:: ASCII Table
                     :name: ascii-table-1

                  *On mobile phones, many binary values listed here will
                  be interpreted as phone numbers. This gives them a
                  blue, clickable link.*

                  ======== ======= === =========================
                  Binary   Decimal Hex Character
                  0000000  0       00  **NULL**
                  0000001  1       01  Start of Heading
                  0000010  2       02  Start of Text
                  0000011  3       03  End of Text
                  0000100  4       04  End of Transmission
                  0000101  5       05  Enquiry
                  0000110  6       06  Acknowledgement
                  0000111  7       07  Bell
                  0001000  8       08  Backspace
                  0001001  9       09  Horizontal Tab
                  0001010  10      0A  **New Line**
                  0001011  11      0B  Vertical Tab
                  0001100  12      0C  Form Feed
                  0001101  13      0D  Carriage Return
                  0001110  14      0E  Shift Out
                  0001111  15      0F  Shift In
                  0010000  16      10  Data Link Escape
                  0010001  17      11  Device Control 1
                  0010010  18      12  Device Control 2
                  0010011  19      13  Device Control 3
                  0010100  20      14  Device Control 4
                  0010101  21      15  Negative Acknowledgement
                  0010110  22      16  Synchronous Idle
                  0010111  23      17  End of Transmission Block
                  0011000  24      18  Cancel
                  0011001  25      19  End of Medium
                  0011010  26      1A  Substitute
                  0011011  27      1B  Escape
                  0011100  28      1C  File Separator
                  0011101  29      1D  Group Separator
                  0011110  30      1E  Record Separator
                  0011111  31      1F  Unit Separator
                  00100000 32      20  Space
                  00100001 33      21  !
                  00100010 34      22  "
                  00100011 35      23  #
                  00100100 36      24  $
                  00100101 37      25  %
                  00100110 38      26  &
                  00100111 39      27  '
                  00101000 40      28  (
                  00101001 41      29  )
                  00101010 42      2A  \*
                  00101011 43      2B  +
                  00101100 44      2C  ,
                  00101101 45      2D  -
                  00101110 46      2E  .
                  00101111 47      2F  /
                  00110000 48      30  0
                  00110001 49      31  1
                  00110010 50      32  2
                  00110011 51      33  3
                  00110100 52      34  4
                  00110101 53      35  5
                  00110110 54      36  6
                  00110111 55      37  7
                  00111000 56      38  8
                  00111001 57      39  9
                  00111010 58      3A  :
                  00111011 59      3B  ;
                  00111100 60      3C  <
                  00111101 61      3D  =
                  00111110 62      3E  >
                  00111111 63      3F  ?
                  01000000 64      40  @
                  01000001 65      41  A
                  01000010 66      42  B
                  01000011 67      43  C
                  01000100 68      44  D
                  01000101 69      45  E
                  01000110 70      46  F
                  01000111 71      47  G
                  01001000 72      48  H
                  01001001 73      49  I
                  01001010 74      4A  J
                  01001011 75      4B  K
                  01001100 76      4C  L
                  01001101 77      4D  M
                  01001110 78      4E  N
                  01001111 79      4F  O
                  01010000 80      50  P
                  01010001 81      51  Q
                  01010010 82      52  R
                  01010011 83      53  S
                  01010100 84      54  T
                  01010101 85      55  U
                  01010110 86      56  V
                  01010111 87      57  W
                  01011000 88      58  X
                  01011001 89      59  Y
                  01011010 90      5A  Z
                  01011011 91      5B  [
                  01011100 92      5C  \\
                  01011101 93      5D  ]
                  01011110 94      5E  ^
                  01011111 95      5F  \_
                  01100000 96      60  \`
                  01100001 97      61  a
                  01100010 98      62  b
                  01100011 99      63  c
                  01100100 100     64  d
                  01100101 101     65  e
                  01100110 102     66  f
                  01100111 103     67  g
                  01101000 104     68  h
                  01101001 105     69  i
                  01101010 106     6A  j
                  01101011 107     6B  k
                  01101100 108     6C  l
                  01101101 109     6D  m
                  01101110 110     6E  n
                  01101111 111     6F  o
                  01110000 112     70  p
                  01110001 113     71  q
                  01110010 114     72  r
                  01110011 115     73  s
                  01110100 116     74  t
                  01110101 117     75  u
                  01110110 118     76  v
                  01110111 119     77  w
                  01111000 120     78  x
                  01111001 121     79  y
                  01111010 122     7A  z
                  01111011 123     7B  {
                  01111100 124     7C  \|
                  01111101 125     7D  }
                  01111110 126     7E  ~
                  01111111 127     7F  Delete
                  ======== ======= === =========================

                  Via the esolangs wiki.

                  .. rubric:: Sources
                     :name: sources

                  ::

                     @atelierbram, Syntax Highlighting Color Schemes: Atelier Schemes. (n.d.) Retrieved July 16, 2022 from 
                     https://atelierbram.github.io/syntax-highlighting/atelier-schemes/
                     -
                     ASCII table. ASCII Table - ASCII Character Codes, HTML, Octal, Hex,
                     Decimal. (n.d.). Retrieved January 16, 2022, 
                     from https://www.asciitable.com/
                     -
                     Bf. Esolang. (n.d.). Retrieved January 16, 2022, 
                     from https://esolangs.org/wiki/Bf
                     (Swear word removed.)
                     -
                     Bellbase. Esolang. (n.d.). Retrieved June 4, 2022, 
                     https://esolangs.org/wiki/Bellbase_Documentation
                     -
                     Davis, S. A. (n.d.). Rear Admiral Grace Murray Hopper.  Retrieved June 12, 2022, from 
                     https://ei.cs.vt.edu/~history/Hopper.Danis.html 
                     -
                     Encyclopedia Britannica, inc. (n.d.). ASCII. Encyclopedia Britannica. Retrieved June 3, 2022, from 
                     https://www.britannica.com/topic/ASCII
                     -
                     Java Data Types. Java data types. (n.d.). Retrieved June 3, 2022, from https://www.w3schools.com/java/java_data_types.asp
                     -
                     Nichols Davis, Coloring for Colorblindness. (n.d.) 
                     Retrieved July 16, 2022 from https://davidmathlogic.com/colorblind/#%23D81B60-%231E88E5-%23FFC107-%23004D40
                     -
                     Truth-machine. Esolang. (n.d.). Retrieved February 2, 2022, 
                     from https://esolangs.org/wiki/Truth-machine
                     -
                     Wikimedia Foundation. (2021, December 25). Extended backus-naur form. 
                     Wikipedia. Retrieved January 17, 2022, 
                     from https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form#Table_of_Symbols
                     -
                     Wikimedia Foundation. (2022, January 4). Turing completeness. Wikipedia. 
                     Retrieved January 16, 2022, 
                     from https://en.wikipedia.org/wiki/Turing_completeness
                     -
                     Wikimedia Foundation. (2022, January 14). Turing machine. Wikipedia. 
                     Retrieved January 16, 2022, 
                     from https://en.wikipedia.org/wiki/Turing_machine
