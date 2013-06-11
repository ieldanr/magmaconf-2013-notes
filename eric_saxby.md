Rails at higher scale

Wanelo

Tracking saturation and utilization.
They use new relic.

Watch queries that are the most often used. This could go into stories.
Average response latency increases over time.

Step 1. Cache everything.
  But cache invalidation!

Cache sweepers worked for them.
Fragments can be shared between pages.

Cache = less queries into database.

Still with cache still Harddrive 100% busy

Counts are problematic. counter_cache.
But there are DEADLOCK errors, which could break your DB.
They put counter cache in a queue with a delayed job. Deduplicate delayed jobs.

Pagination doing counts!  They did a monkey patch on Kaminari so that it gets directly the counter.

How do we really know what rails is actually doing?
* ruby-prof
    showed URLS generation is very slow.
* pilfer

Removing RABL
inefficient :to_json

rendering JSON partials should hash.merge!

What happens when you data grows larger than a single DB
Service Oriented Application.

You should not try to improve it with one deploy. But iterate on it.
Do tests.

Takeaways.

Choose technologies that are easy to operate and monitor.
POSTGRES > mysql

Assume that data should be tracked, even if you don't understand the relevance.

Small iterative performance improvements can have massive payoff over time.

Uitlization:
  Reads easier to scale than writes. Read/write splitting, caching.

When writes become a bottle neck then services is one of the answers.
Microsecond delays can reduce load, depends on application.


