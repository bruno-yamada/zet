# Respect your legacy (code)

It is very common to find teams that complain about "legacy" code and blame
issues on "legacy" code, this has always felt weird, because it makes it seems
like "legacy" is a bad thing, but isn't "legacy" code what brought the
organization this far?

## Legacy Code is often underestimated

I was at this company once, which has been going on for at least five years at
that time, and had this application developed in PHP, which was its main
product, and them a new "senior developer" joined.

The leadership put high hopes on him, given the experiences of this resume and
his "soft skills". In his first week, the tech
leads of each area of the company where required to have a meeting with him,
where they would explain the intricacies of the application, how it all
connected together and the reasoning behind it, the application although
developed only in PHP was pretty large, used SQL and NoSQL databases, had
websockets and the frontend was that of a SPA (Single Page Application).

There where many discussions between him and the team, where they would find
points that could be improved, amongst which was: moving from a PHP application to
a NodeJS one, breaking the application down into microservices, maybe making it
serverless, and change the way websockets were used. Those ideas have always
been in the head of those tech leads, and as such, they were pleased to hear him
validate their thoughts, but of course, those changes would require time and
buy-in from the upper levels, and it is always difficult to push for "improving
the application" from a technical point of view, when you could just be
developing more features to bring in potentially more paying customers.

At the end of that week, over the last meeting with the tech leads, that
"senior developer" said:

> _I can work on this and re-write the application over the weekend_

Now think about how much that means, needless to say the tech leads just
laughted it off, in saying that, not only did he diminished all the hours of work they
have already done in the application, but also severely underestimated the
complexity of it.

The weekend went by, the "senior developer" didn't show anything on monday,
another week went by, nothing was shown yet again, after 4 months of work, of
both him and a small team with other 3 developers they had a very subpar proof
of concept, not ready to replace the entire application, but to only a small
portion of it.

## Legacy Code has a lot of man-hours invested

Often we come across huge legacy projects, with thousands upon thosands of lines
of code, spanning over many years of active development, bug fixes, features
implemented and edge cases considered. All of that work was done in a way, for a
reason, and it is not uncommon that when you try to refactor or rebuild some
piece of legacy code, you end up coming against some issue and then you think:

> _"ha! now I know why they did it like that!"_

## Legacy Code is not untouchable

Dealing with a legacy project does not mean you cannot refactor it, improve it
or slowly decommission it.

There was this "legacy" project that was a simple java application, but very
important to the workings of a certain company I worked at. It existed in a
windows virtual machine, and was started using plain old `java -jar` manually.
Over the course of a couple days, we extract that java application into a
container of its own, which we could then deploy in our kubernetes cluster, and
that gave us many benefits such as being able to scale its resources more
easily, having more than one instance of the application running simultaneously,
having it automatically restart if it should fail for some reason and many other
benefits naturally provided by using containers and kubernetes.

So, what we did wasn't necessarily changing the code of the application, just
how it was being "deployed", but that gave us a lot of benefits and made that
part of the company specifically way less suceptible to faults.

Another good approach is to slowly break apart funcionatilities of the legacy
application, maybe by extracting some part that is a bottleneck to performance,
careful analysis of the inner workings and an atomic approach is advised.

## There are exceptions

I once worked in this company, it was very up-to-date with its technologies, it
was using Kubernetes, with CI/CD pipelines, proper logging, monitoring, code
scanning, and most of the latest practices for maintaining and delivering code.
But it didn't come easy, and was a movement that took 2 to 3 years, there were
many projects that had to be migrated, and the changes and adoptions where made
slowly over that period.

And then, there was this project, it was resistant to all the changes going on
in the company, it didn't follow the kubernetes train. The project itself was
about 3 years old, always had active development, but the developers didn't want
to change or learn, in fact, it could probably be consider a legacy project in
the way it was developed from the moment it was born.

The project was a Drupal application, that used very outdated modules, most of
what was done in the Drupal, could easily be replaced by simple static page
websites, deployments were done by developers entering through SSH into
production servers and running `git pull`, so even when talking about the most
up-to-date ways of handling Drupal websites, this project was way outdated.

So there are a few cases where legacy projects happen and don't make much sense,
maybe it is due to lack of skill from the team responsible, maybe it is lack of
time or interest for properly maintaining it, who knows.

I didn't get a chance to talk with the developers, only heard of the project
through a fellow DevOps, and don't know what happened to the project after I
left the company, last I checked, they were still using the same old Drupal
installation with, maybe hopefully they changed the way they did deployments.

## Just come from a place of respect

We, as programmers, developers, hackers, coders, or whatever is the new
buzzword, have big egos, but when looking at "legacy code", take a step back and
think about the reasons why a project was developed in a certain way.

> tags: legacy-code; development;

> uid: 20210928090524Z

> links:
