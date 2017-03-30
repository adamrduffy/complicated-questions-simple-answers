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

list vs set

comparator and comparable

tile definitions

spring annotations

junit annotations

double null check

synchronized

constants and static final

# Groovy

avoid null pointer exceptions
