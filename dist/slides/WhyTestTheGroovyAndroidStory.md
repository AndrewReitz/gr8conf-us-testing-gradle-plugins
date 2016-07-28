# Why Test (The Groovy Android Story)

Groovy Android Plugin has many dependencies

| Java Version | Gradle Version | Android Build Tools Version |
| :-----------:|:--------------:|:---------------------------:|
| 1.6          | 2.10           | 1.1.0                       |
| 1.7          | 2.11           | 1.3.0                       |
|              | 2.12           | 1.5.0                       |
|              | 2.13           | 2.0.0                       |
|              | 2.14           | 2.1.2                       |

Note:
So these are just some of the external dependencies that the Groovy Android Plugin
has. The things listed out here are just the dependencies I currently test against
these areas have been identified as areas that has breaking changes or notable
changes that have different effects on the plugin, and this matrix is all
interchangeable which leads to a lot of areas that could go wrong.

Also something to note that the build tools have external dependencies. Which
some even depend on gradle. There was an issues with some of the 1.x dependencies
where you use to need gradle 2.2 or less. But with an update to the underlying
dep they then required 2.10 or greater.

Also other things need to be tested to ensure they work (some android voodoo magic)
such as databinding, and renderscripit. These are just freatures people have reported
as not working, and I'm sure there are other things out there that haven't even
been reported yet. So the moral of the story is, there is a LOT of things that
this single plugin has to manage, and testing them all by hand to ensure I didn't
break anything would suck.
