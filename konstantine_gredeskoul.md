Accelerating WANELO from 5K to 200K RPM in 6 Months
by Konstantine Gredeskoul
CTO Wanelo.

Thoughts on system architecture...

8 M users
6 M products saved 1 B times
8 M products saved per day
200k stores
4 codebases: chef, ruby-web, iOS, Android
10 engineers, pairing + TDD full-time

06/2012 RoR App Relaunches RPM 2-3K
08/2012 iOS App is launches 5-20K
12/2012 Android app launches 40-120K
03/2013 #24 top free on iTunes 60-200K

Stack
MRI RUby 1.9.3 & Rails 3.2
PostgreSQL, Solr
Joyent Cloud, SmartOS
CIrconus, NewRelic, Boundary (Monitoring, alerting)
Chef + Opscode
Amazon S3...

Last year magmaconf 2012 Enterprise architecture with ruby (and rails).

Small scale - heroku
large scale - putting things together is hard.

What makes a good Systems Architecture.
Let's start with simply "good" software design.
Well designed software is a software that's easy to change -- Dave Thomas

To achieve that, weel designed software is often modular, decoupled and test covered.

Well designed systems architecture:
  Easy to scale up or down with demand
  Easy to deploy monitor and diagnose
  Highly available
  Fault tolerant (or easy to recover)
  Cheap(ish) to run
  Fast (low latency to web requests)

It's always about the trade-offs.

nginx -> haproxy (Load balancer)
Unicorn sidekid.

New relic rocks!

Remove application latencies.


