Creating APIs with Hypermedia
========
by Javier Cervantes from Hybrid Group
--------

Basically Hypermedia means adding URLS of the business logic to the API responses.
This way the user can navigate through the API using the added links.

Example:

    {
      "_links": {
        "self": {
          "href": "/states/arkansas"
        },
        "next": {
          "href": "/states/california"
        },
        "previous": {
          "href": "/states/arizona"
        },       
        "US_Senators": [
          "senior": {
            "href": "/states/arkansas/senators/jsmith/"
          },
          "junior": {
            "href": "/states/arkansas/senators/bclinton/"
          },
        ]
    },
    "population": 1234567,
    "state_flower": "rose"
    }

One good advantage from doing this is not having to use ID's anymore. One could do:

      client.get(response[:person][:url])
      
Instead of:

      client.get("/people/#{response[:person][:id]}")

More resources
----------

#####Presentation

https://speakerdeck.com/solojavier/creando-apis-con-hypermedia

####Explains more about why Hypermedia

http://stackoverflow.com/questions/15214526/why-hypermedia-api


#####Interesting article about hypermedia

http://37signals.com/svn/posts/3373-getting-hyper-about-hypermedia-apis

Talks that it is nice to use URLs instead of IDs for the calls. but says that at the moment it doesn't serve much




