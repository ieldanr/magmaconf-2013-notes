Apps web 2.0, API's with RoR and frontend with EmberJS
===========
by Edwin Cruz from Crowd Interactive
------------

###APIS and EmberJS: API best practices

####REST + CRUD
####API VERSIONING METHODS
  * Namespaces
    * /int/url
    * /ext/url
    * /pub/url 
  * Version number
    * v2/url
  * On URL
    * pub.api.com  
  * On ideal world it should be on HEADER
      
####HTTP CODES
  Use error codes correctly for each of the different cases.

###Better API's

  * Reduce number of requests
  * DRY - Dont repeat yourself
  * Caching - Include a version in the api. Russian Doll Caching.
      * Counter Caches
      * Caching with Solr (Sunspot interface for ruby)

###EmberJS
  Javascript Framework for creating ambitious web applications
  
  Problems that solves:
  
  * Data binding
  * Real time updates
  * Performance
  * Patterns
  * Scalability

We might need to update things in many places. EmberJS can help us.
  
Structure:
  * Models
    * ORM, Transactional.
  * Observers
    * **property** Computed properties
    * **observes** react when something happens
    * **bindings** Makes sure everything is synched
  * Router
    * EmberJS way for managing states.
