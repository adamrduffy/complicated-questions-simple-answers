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

## What are the keys differences between Comparable and Comparator.

When your class implements Comparable, the compareTo method of the class is defining the "natural" ordering of that object. That method is contractually obligated (though not demanded) to be in line with other methods on that object, such as a 0 should always be returned for objects when the .equals() comparisons return true.

A Comparator is its own definition of how to compare two objects, and can be used to compare objects in a way that might not align with the natural ordering.

For example, Strings are generally compared alphabetically. Thus the "a".compareTo("b") would use alphabetical comparisons. If you wanted to compare Strings on length, you would need to write a custom comparator.

In short, there isn't much difference. They are both ends to similar means. In general implement comparable for natural order, (natural order definition is obviously open to interpretation), and write a comparator for other sorting or comparison needs.

http://stackoverflow.com/a/4108764

## What does 'synchronized' mean?

When you have two threads that are reading and writing to the same 'resource', say a variable named foo, you need to ensure that these threads access the variable in an atomic way. Without the synchronized keyword, your thread 1 may not see the change thread 2 made to foo, or worse, it may only be half changed. This would not be what you logically expect.

http://stackoverflow.com/a/1085745

### Double-checked locking

If you need to use lazy initialization for performance on an instance field, use the double-check idiom. This idiom avoids the cost of locking when accessing the field after it has been initialized (Item 67). The idea behind the idiom is to check the value of the field twice (hence the name double-check): once without locking, and then, if the field appears to be uninitialized, a second time with locking. Only if the second check indicates that the field is uninitialized does the call initialize the field. Because there is no locking if the field is already initialized, it is critical that the field be declared volatile (Item 66).

http://stackoverflow.com/a/3580658

## How to declare a constant in Java?

You can use an enum type in Java 5 and onwards.

Use the final modifier on a field in a class or declare a field in an interface.

### What are enums and why are they useful?
You should always use enums when a variable (especially a method parameter) can only take one out of a small set of possible values. Examples would be things like type constants (contract status: "permanent", "temp", "apprentice"), or flags ("execute now", "defer execution").

If you use enums instead of integers (or String codes), you increase compile-time checking and avoid errors from passing in invalid constants, and you document which values are legal to use.

http://stackoverflow.com/a/4709224

## Tiles

Tiles allows authors to define page fragments which can be assembled into a complete page at runtime. These fragments, or tiles, can be used as simple includes in order to reduce the duplication of common page elements or embedded within other tiles to develop a series of reusable templates. These templates streamline the development of a consistent look and feel across an entire application.

Declared in tile definition file where each definition may have one or more attributes.

https://tiles.apache.org/framework/

## Spring

### Context Configuration Annotations
@Autowired - Declares a constructor, field, setter method, or configuration method to be autowired by type. Items annotated with @Autowired do not have to be public.
@Configurable - Used with <context:springconfigured> to declare types whose properties should be injected, even if they are not instantiated by Spring. Typically used to inject the properties of domain objects.
@Order - Defines ordering, as an alternative to implementing the org. springframework.core.Ordered interface.
@Qualifier - Guides autowiring to be performed by means other than by type.
@Required - Specifies that a particular property must be injected or else the configuration will fail.
@Scope - Specifies the scope of a bean, either singleton, prototype, request, session, or some custom scope.

### Stereotyping Annotations
@Component - Generic stereotype annotation for any Spring-managed component.
@Controller - Stereotypes a component as a Spring MVC controller.
@Repository - Stereotypes a component as a repository. Also indicates that SQLExceptions thrown from the component's methods should be translated into Spring DataAccessExceptions.
@Service - Stereotypes a component as a service.

### Spring MVC Annotations
@Controller - 

https://dzone.com/refcardz/spring-annotations

junit annotations

# Groovy

avoid null pointer exceptions
