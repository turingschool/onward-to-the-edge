Onward To The Edge!
===================

An assortment of projects to move us onward to the edge.

https://www.youtube.com/watch?v=akek6cFRZfY


Purpose
-------

Push the horizons of our capability.<br />
Increase our knowledge and experience.<br />
Explore the foundations we build upon.<br />
Struggle and overcome.<br />
Indulge curiosity.<br />
Discover.<br />
Play.<br />

## Status

Many of these are just ideas without a project to go along with them.
If you find one interesting, let me know and we'll fill out the
specification and requirements.

## Data Structures and Algorithms

Data structures are the ways that we structure data in memory
in order to represent information in a useful way.

Sometimes "useful" means it accurately reflects realworld data.
for example, a user in our system might have a name and age,
so the data structure to represent that might be a hash with the key
"name" mapping to a string, and the key "age" mapping to an integer.

Other times "useful" means that the structure has certain properties
that meet our needs. For example, an array is a data structure that
gives us random access to elements in a collection (we can access
any element directly), and a list is a data structure that gives us
sequential access to elements (to access the fifth element, we must go
through the first four).

In order to take advantage of the properties of these data structures,
the computer will need to execute a series of instructions which
achieve a goal. This series of instructions is called an algorithm.
Hence, data structures often come with a set of algorithms to make
use of their properties.

Other times, an algorithm is not tied to a data structure.
It simply achieves a useful goal for us.

We will explore common data structures, their algorithms,
and other algorithms in this section.

* Calculations
  * [Luhn algorithm](https://github.com/turingschool/data_structures_and_algorithms/tree/master/luhn_algorithm)
    difficulty: low<br />
    An algorithm used to validate credit card numbers
  * [MD5](https://github.com/turingschool/data_structures_and_algorithms/tree/master/md5)
    difficulty: medium<br />
    A hashing algorithm -- takes a piece of data in binary format,
    and traverses through it, performing calculations as it goes,
    For example, running Mac OSX's md5 program against itself:
    ```sh
    $ md5 `which md5`
    # >> MD5 (/sbin/md5) = d1ec2c37a8815b004f4db736f8b766be
    ```
    If your computer comes out with the same value, then the assumption
    is that you and I have the same program (it is bit-for-bit equivalent).
  * Pseudorandom number generator (middle squares method)<br />
    The algorithm described in [this](https://www.youtube.com/v/FfZurPKYM2w?start=350) video.
    A Wikipedia [article](https://en.wikipedia.org/wiki/Middle-square_method).
* Collections
  * [Linked lists](https://github.com/turingschool/data_structures_and_algorithms/tree/master/linked_lists)
    difficulty: low<br />
    Any collection where each element contains a reference to the next element.
    These are the fundamental building blocks of lisp.
    While their representation may change, they are ubiquitous.
    For example, a group doing a secret santa is a linked list.
    I will buy a gift for you, and you will buy a gift for the next person,
    who will buy a gift for the next person, etc.
  * [Binary Search Tree](https://github.com/turingschool/data_structures_and_algorithms/tree/master/binary_trees)
    difficulty: medium<br />
    Any collection where each element has a reference to two other elements,
    called "left" and "right", and no elements have more than one link pointing to them.
    If the tree is balanced (each element has the same number of elements down its left branch,
    as it does down its right branch), then this allows you to remove half the number
    of elements every time you go down a path. Hence, it can be used to very quickly
    search for items (in a tree with 1 million nodes, you'd have to look at fewer than 20
    before finding the one you wanted).

    This can be implemented either with "nodes", like a linked list,
    or with arrays.
  * [Heap](http://en.wikipedia.org/wiki/Heap_%28data_structure%29)
    difficulty: medium<br />
    If you're interested in this, let me know and I'll fill it out.
    A heap is a tree data structure with the property that each of its
    elements is greater than any of its children (or less than any of its children).
    It can be implemented with nodes like a linked list, or with arrays.
  * Immutable doubly linked list (difficulty: high)<br />
    A doubly linked list has references both forwards and backwards.
    The extra constraint of immutability means that none of the nodes may be changed.
    So if you have a reference to one of these lists, you can be confident that it
    cannot be modified by anyone you pass it to. This is accomplished primarily by
    creating new lists for each operation. There are primarliy two challenges:
    to actually make the thing, and to make it efficient. The first isn't that hard
    in a language like Ruby, but if you accept the constraints of a language like Haskell,
    it becomes significantly more difficult.
  * ArrayList in C (difficulty: high)<br />
    Wikipedia [article](https://en.wikipedia.org/wiki/Array_list).
    This is high, primarily because you are operating in C.
    The arrays you get to use in Ruby are wonderful.
    You can push more elements in them, you can pop elements out of them.
    This is really an `ArrayList`. At lower levels of abstraction, there
    is no such thing, you only have the address of a piece of contiguous
    memory. That's it. This challenge will require you to operate at a
    C level, creating functions that provide all the abstractions Ruby
    gives you.

    An interesting extension might be to then make your ArrayList
    available from Ruby.
* Sorting<br />
  If you're interested in any of these, let me know and I'll fill out the details.
  * Bubble sort
  * Insertion sort
  * Selection sort
  * Quick sort
  * Heap sort
  * Merge sort
* Graphs
  * [A\*](https://github.com/turingschool/data_structures_and_algorithms/tree/master/a_star)
    difficulty: medium<br />
    A\* is an algorithm for searching when searching is difficult because either
    the search space is so large (possibly infinite) that you can't
    check all the options to see if any of them work (e.g. the number of chess games
    where player 1 wins).
    In this case, it searches to a out a given depth,
    and analyzes the element there, attempting to identify whether it is favourable.
    This attempt is called a heuristic, and it A\* works by moving towards the element
    with the best heuristic at the edge of its horizon.
    Thus, it's rather similar to a game of warmer/colder.
  * [Pathfinding](https://github.com/turingschool/data_structures_and_algorithms/tree/master/pathfinding)
    difficulty: medium<br />
    In this challenge, you will be given a maze ([example](https://github.com/turingschool/data_structures_and_algorithms/blob/25b7e0080198d26ce75ea0970deadb496d0a62ba/pathfinding/test/fixtures/landscape1.txt)),
    and must locate a path from the start to the finish.

## The internet

An internet is a collection of computer networks.
"The Internet" is the global collection of networks
that we all connect to to visit a website, view our email, etc.
It is common to do work on the internet without understanding
the layers you're building on top of. This set of projects
is intended to explore these layers.

* [Build a webserver](https://github.com/wrightcheek/build-a-webserver)
* Build Rack
* Build Sinatra

## Your own Core Ruby

* Create your own Array (difficulty: medium)<br />
  You will need to implement your own Array class,
  and all interesting methods from the real Array class.
  You can do this either by building it on top of a linked list,
  or by making your own ArrayList at the C level and making
  it available in Ruby (these are both other projects in this directory).
* Create your own Hash (difficulty: medium)<br />
  Ruby provides you a convenient `Hash` class, and nice literals
  (the syntax `{a: 1}`) to create them. In this project, you will
  not have access to Ruby's Hash, you will need to construct your own.
  This project cam be combined with "Create your own Array" for
  the especially awesome knowledge that you have built everything you are using..
  A possible extension is to make it ordered, like Ruby's hashes
  (normally hashes have no ordering.)
* Create your own Set (difficulty: low)<br />
  A set is a data structure like an array,
  except it has no ordering,
  and anything which could potentially be an element,
  either is or isn't (the elements are unique, because it is
  meaningless to say an element is in the set multiple times).
  This project can be combined with the "Create your own Hash"
  project above.
* Create your own Enumerable and Enumerator (difficulty: high)<br />
  What better way to understand Enumerable and Enumerator than to build them?
  You can then include them into your own collections.
  This project can be combined with any of the three above to
  allow you to include your own `Enumerable` into your own `Array`,
  `Hash`, and `Set`.
* Create your own String (difficulty: unknown)<br />
  A string is a sequence of characters. A character is typically
  represented with a number. For example:
  ```ruby
  "a".ord  # => 97
  97.chr   # => "a"

  [104, 101, 108, 108, 111, 32, 119, 111, 114, 108, 100].each do |ascii_value|
    $stdout.putc ascii_value
  end
  # >> hello world
  ```
  You will need to create your own `String` class by internally
  keeping an array of numbers which correspond to these characters.
  You will need to implement any interesting methods from the `String`
  class for your collection.
* Build your own gem

## Terminal

* ANSI escape values<br />
  Do you know how to colour text on the terminal?
  ```sh
  $ ruby -e 'puts "\e[31mTHIS IS RED\e[39m"'
  ```

  And how does `clear` clear your screen?

  ```sh
  $ clear | ruby -e 'p $stdin.read'
  "\e[H\e[2J"
  ```

  Try it yourself:

  ```sh
  $ ruby -e 'print "\e[H\e[2J"'
  ```

  Construct a library that gives you methods to do anything
  interesting on the terminal. [Here](https://en.wikipedia.org/wiki/ANSI_escape_code)
  is a nice list. You can do things like change colours,
  and move the cursor around.
* 256 color mode<br />
  Despite the low number of colours you frequently see,
  many terminals (e.g. if you are using iTerm) support up to 256
  colours. There is a mapping to allow you the ability to specify
  each colour based on RGB values (the amount of red, green, and blue
  in the colour).
  * Create a program to display all of these colours
  * Write the algorithm that translates a given RGB value into
    an escape sequence you can use to colour your output
  * Create a program that takes an image and draws it in the terminal
    by setting the background colour as close as possible, and
    writing spaces.
    [Example](https://github.com/JoshCheek/print-png/blob/52188a8c19b9633ca420b927a55ea8229b174588/screenshot-rainbow.png)
