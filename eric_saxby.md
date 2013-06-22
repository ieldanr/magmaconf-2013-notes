Scaling Wanelo 100x
======
by Eric Saxby from Wanelo
------

They scaled their rails app to do 200K requests per minute (RPM) in six months. The slides talk about how they did it.

Here are the slides http://building.wanelo.com/

####New Relic
For tracking saturation and utilization.

Watch queries that are the most often used. This could go into stories. Average response latency increases over time.

####Cache everything.

But watch out for cache invalidation!

Cache sweepers worked for them.

Fragments can be shared between pages.

Cache = less queries into database.

They found out that still with cache the HD was always busy at a 100%

They also do counter caches!

####How do they really know what rails is actually doing?
* ruby-prof
    
  They learned using ruby-prof that URLS generation was very slow.

####What happens when you data grows larger than a single DB

You start to do a Service Oriented Application.

One of the lessons they give is to always iterate. Never try to fix everything with one deploy.

####Takeaways

Choose technologies that are easy to operate and monitor.

POSTGRES > mysql

Assume that data should be tracked, even if you don't understand the relevance.

Small iterative performance improvements can have massive payoff over time.

Reads easier to scale than writes. Read/write splitting, caching.

When writes become a bottle neck then services is one of the answers.

Microsecond delays can reduce load, depends on application.


