# Brain Teasers

cycle detection in linked lists - floyd's algorithm - tortoise and hare

http://stackoverflow.com/a/6110767


fibonacci algorithm - recursion and iteration

# REST

idempotent PUT and POST

# Java

## What are the differences between a HashMap and a Hashtable in Java?

There are several differences between HashMap and Hashtable in Java:

Hashtable is synchronized, whereas HashMap is not. This makes HashMap better for non-threaded applications, as unsynchronized Objects typically perform better than synchronized ones.

Hashtable does not allow null keys or values.  HashMap allows one null key and any number of null values.

One of HashMap's subclasses is LinkedHashMap, so in the event that you'd want predictable iteration order (which is insertion order by default), you could easily swap out the HashMap for a LinkedHashMap. This wouldn't be as easy if you were using Hashtable.

http://stackoverflow.com/a/40878

## What is the difference between the Set and List interfaces?

List is an ordered sequence of elements whereas Set is a distinct list of elements which is unordered.

List

An ordered collection (also known as a sequence). The user of this interface has precise control over where in the list each element is inserted. The user can access elements by their integer index (position in the list), and search for elements in the list.

Set

A collection that contains no duplicate elements. More formally, sets contain no pair of elements e1 and e2 such that e1.equals(e2), and at most one null element. As implied by its name, this interface models the mathematical set abstraction.

http://stackoverflow.com/a/1035012

comparator and comparable

tile definitions

spring annotations

junit annotations

double null check

synchronized

constants and static final

# Groovy

avoid null pointer exceptions
