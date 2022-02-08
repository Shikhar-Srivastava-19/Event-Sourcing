# Event Sourcing
## What is it?

Events represent the transition of the state of things that have occurred in the system.
The process behind reaching where we are, the storing of steps used in the process to achieve the final destination as data is Event Sourcing. 

Event Sourcing measures that the changes made to my application state are stored as a sequence of events. Not only we can examine these events, but we can also use the event log for subsequent changes and recreate the past log of states.

# How it Works

To ensure that all the changes that occur simultaneously in a process are stored in an event object and that these are sequenced in a manner that they occurred as is Event Sourcing.

Let's consider an example of the lorry. In this, we have many trucks or lorry traveling to various places, and we need to know the exact location to where they are. For this, we have a tracking application that enables us to find the record of when a truck arrives or leaves the transportation center.

In this scenario when a tracking service is called, it finds the relevant truck and updates its whereabouts. Event Sourcing creates an event object to record all the subsequent changes made and further process it to the lorry. We have a record of all the changes that are being made. With Event Sourcing not only do we have the details of the whereabouts of our lorry but also where it has been. We can keep a record of all the places the lorry has stopped by and when it started moving.

# Advantageous

Event Sourcing is a method in which all changes are made by the event objects. This provides us with several functions:
- *To Rebuild completely*: We do not need to look into the current state of the application and rebuild it by examining all the events from the event log.
- *Physical Query*: We can determine the state of our application at any point in time. We can do this by running the event log from scratch up to a particular time or event which is required.
- *Event Replay*: If we see that a past event was incorrect, we could change the event by reversing it and later events and then forming a new set of events according to the log, or if the order of the sequence is in a wrong sequence we could use the same method to set a new set of events.

# Need of Event Sourcing Architecture

Event Sourcing increases the overall scope of the architecture, to be specific if we require something accessible. There is a wide scope of 'event-driven architecture' as of today. Most of the product-based companies need to have a log of a lot of items for example number of orders, packages shipped, packages delivered, shipping status, items in the inventory, an archive folder of the past items sold. Communicating through event messages provides an extremely great track of records and reduces the fragility of system failures.

# Refrences

1.[*https://microservices.io/patterns/data/event-sourcing.html*]

2.[*https://codeopinion.com/event-sourcing-example-explained-in-plain-english/]

3.[*https://martinfowler.com/eaaDev/EventSourcing.html]
