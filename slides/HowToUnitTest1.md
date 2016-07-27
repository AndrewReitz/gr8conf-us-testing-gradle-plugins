# Testing Your Plugin with Unit Tests

## Step one Write Unit Tests

![party parrot](image/parrot.gif)

Note:
Where to start? Before I started changing anything in the groovy android Plugin
I wanted to get tests around the current functionality.

For classes that are not directly related to gradle, services or whatever else
you might have for making your code modular, you can use JUnit or Spock like
you normally would test that class.

Otherwise in my case there were two types of tests. Tests that directly check
small units of work on the extension class and the plugin class. Then there
is the functional/integration tests. I am grouping these two together since
they are both testing the plugins functionality with the other dependencies
that the project requires.

So the first, and probably the easiest tests to get started with are the Unit
Tests.
