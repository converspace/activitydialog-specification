Activity Dialog Specification
=============================

A method for third-party sites to invoke an activity dialog on the users website to allow the user to perform an activity (like, follow, comment, share, etc.) on the third-party owned URI addressable resource on thier own website.

Third-party sites will allow actions (follow, like, comment, share) on their resources by asking for your URI from where they can `GET` an Activity-Dialog URI header that they can popup in a separate window passing in the required parameter (actor, verb, object, etc.). Since this URI is on the users website, it will authenticate the user and the action therefore will happen on the users site and send an [Activity Pingback](http://activitypingback.org/) to the thrid-party website about it. This is kinda like a bookmarklet to a URI on your website that is automatically invoked by a third-party website.

This could also be implemented as a bookmarklet that parses a microformats on the resource it is invoked on and presents all possible actions allowed on that resource.