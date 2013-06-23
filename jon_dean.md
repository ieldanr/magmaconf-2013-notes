Inter-Application communication using secure API's
========
by Jon Dean
--------

Code interfaces
Web APIs

He had Multiple Rails applications that need to share functionality.

There is two ways to communicate between the systems:

* Set up a restful API 
* Gems 
 
At first they made lots of gems to communicate :/ OMG

When there are more systems communicating with each other, that means doing
many many gems! (which is bad...)

Gems
----

####PROS
  * Easy
  * Abstract the work through code-level APIs
  * Can cost less money
  * No network latency
  * No need to implement authentication

####CONS
* Need to update and deploy all applications when the gem changes.
* Lots of code churn/branches
* Internal improvements require a change in all applications using it.

API Service
---
####PROS
* Internal changes have no affect on client apps
* Can independently scale the resource that deals with payments
* Can add clients in any language to your systems

####CONS
* More complex
* Costs money to run an additional application
* Network latency
* Handling timeouts and other service unavailability issues
* Also need to implement an authentication layer

The presentation with an awesome example of versioning:

https://github.com/jonathandean/magmaconf-2013-inter-app-api


