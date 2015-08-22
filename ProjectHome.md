If you'd like to run a site like [Stack Overflow](http://stackoverflow.com), for example on your company's intranet for internal use by developers, keep an eye on this project, which aims to implement a Stack Overflow-like site in Django.

## Planned Features ##

SOClone will make use of [Progressive Enhancement](http://en.wikipedia.org/wiki/Progressive_enhancement) to ensure that all core functionality is available regardless of whether or not the user has JavaScript enabled - some of Stack Overflow's core functionality such as voting, accepting answers, viewing comments, marking questions as favourites and flagging questions as offensive currently doesn't work _at all_ without JavaScript enabled.

Another usability issue which will be fixed is that the lack of submit buttons on some search pages means they can't be used in browsers whose input method does not support typing events, such as Opera on the Nintendo Wii.

Over and above the basic Stack Overflow functionality, SOClone will (eventually) also include an intranet mode, which will tweak the application to be more suitable for use in intranets, with changes such as:

  * LDAP authentication / other pluggable registration/login backends
  * Lowering reputation barriers to access functionality or totally removing reputation from the equation in terms of what you're allowed to do on the site
  * Removing offensive flags
  * Optionally disabling down voting
  * Intranet-specific badges

## Pluggability ##

SOClone does not currently aim to be pluggable in any way, because:

  1. Being pluggable means playing nice...
  1. ...playing nice takes a little longer...
  1. ...the author doesn't currently have the time to take a little longer :)

As a result, you'll see such horrors as hard-coded table names in SQL queries and new fields monkeypatched into the `django.contrib.auth.models.User` model.

The initial goal is to produce something which can be deployed as a standalone application on an intranet.