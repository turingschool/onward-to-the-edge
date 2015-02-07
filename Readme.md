Onward To The Edge
==================

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
  * `luhn_algorithm` difficulty: low<br />
    An algorithm used to validate credit card numbers
  * `md5` difficulty: medium<br />
    A hashing algorithm -- takes a piece of data in binary format,
    and traverses through it, performing calculations as it goes,
    For example, running Mac OSX's md5 program against itself:
    ```sh
    $ md5 `which md5`
    # >> MD5 (/sbin/md5) = d1ec2c37a8815b004f4db736f8b766be
    ```
    If your computer comes out with the same value, then the assumption
    is that you and I have the same program (it is bit-for-bit equivalent).
* Collections
  * `linked_lists` difficulty: low<br />
    Any collection where each element contains a reference to the next element.
    These are the fundamental building blocks of lisp.
    While their representation may change, they are ubiquitous.
    For example, a group doing a secret santa is a linked list.
    I will buy a gift for you, and you will buy a gift for the next person,
    who will buy a gift for the next person, etc.
  * `binary_search_trees` difficulty: medium<br />
    Any collection where each element has a reference to two other elements,
    called "left" and "right", and no elements have more than one link pointing to them.
    If the tree is balanced (each element has the same number of elements down its left branch,
    as it does down its right branch), then this allows you to remove half the number
    of elements every time you go down a path. Hence, it can be used to very quickly
    search for items (in a tree with 1 million nodes, you'd have to look at fewer than 20
    before finding the one you wanted)
  * `a_star` difficulty: medium<br />
    A\* is an algorithm for searching when searching is difficult because either
    the search space is so large (possibly infinite) that you can't
    check all the options to see if any of them work (e.g. the number of chess games
    where player 1 wins).
    In this case, it searches to a out a given depth,
    and analyzes the element there, attempting to identify whether it is favourable.
    This attempt is called a heuristic, and it A\* works by moving towards the element
    with the best heuristic at the edge of its horizon.
    Thus, it's rather similar to a game of warmer/colder.
* Graphs
  * `pathfinding` difficulty: medium<br />
  In this challenge, you will be given a maze ([example](https://github.com/turingschool/data_structures_and_algorithms/blob/25b7e0080198d26ce75ea0970deadb496d0a62ba/pathfinding/test/fixtures/landscape1.txt)),
  and must locate a path from the start to the finish.

## The internet

An internet is a collection of computer networks.
"The Internet" is the global collection of networks
that we all connect to to visit a website, view our email, etc.
It is common to do work on the internet without understanding
the layers you're building on top of. This set of projects
is intended to explore these layers.

* build your own webserver repo       - https://github.com/wrightcheek/build-a-webserver
* build your own rack                 -
* build your own Sinatra              -

## Concurrency

* Threads - https://github.com/JoshCheek/event_loop

