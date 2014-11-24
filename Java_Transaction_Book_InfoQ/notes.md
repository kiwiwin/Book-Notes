#Chapter 8 Domain Service Owner Transaction Design Pattern

most widely used

##Context

Service layer should be responsible for managing transactions:

1. we may not know the type of client accessing the backend services(so?)
2. too much burden for client
3. performance suffers

Java applications are usually designed with *mid-* to *course-grained* domain service
(why mid- to course-grained?)

##Forces

1. client make a single request
2. ACID
3. domain service objects are course-grained and/or use inter-service communication to perform aggregate service requests

##Solution

places the entire responsibility of transaction management on the Domain Services

1.Transaction Attribute [Requried] for all insert, update, delete methods.

[Required] is used for the Domain Service components rather than [RequiresNew] transaction attribute in the inter-service communication is used between Domain Service components(something is fairly common in most enterprise java application).

**DILEMMA**: Inter-service Communication



2.Transaction Attribute [Supports] fro all read operations


##Consequences

…

#Chapter 9 Server Delegate Owner Transaction Design Pattern

This transaction is most applicable when using the Command Pattern or Server Delegate Design Pattern in your application architecture.

