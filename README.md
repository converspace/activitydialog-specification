ActivityDialog Specification
=============================

A method to open an ActivityDialog, a resource that the user controls, that allows them to create an activity stream entry on their website, the object of which can be any URI addressable resource. This could be implemented as a simple bookmarklet that prefills the object of the activity with the current URL and/or the selected text as content. 

The activity stream entry should trigger an [ActivityPush](http://activitypush.org/) to the object and a PubSubHubbub push for followers.

## Ideas:
* Plugins could add behaviour for know URI spaces (liking a facebook link should trigger a facebook like, sharing a twitter link should trigger a retweet)?
* Plugins could add behaviour to verbs (liking a link could bookmark it, following could send a pubsubhubbub sub request)?

## Older stuff

* A method for third-party sites to invoke an ActivityDialog on the users website to allow the user to perform an activity (like, follow, comment, share, etc.) on the third-party owned URI addressable resource on thier own website.

* Third-party sites will allow actions (follow, like, comment, share) on their resources by asking for your URI from where they can `GET` an Activity-Dialog URI header that they can popup in a separate window passing in the required parameter (actor, verb, object, etc.). Since this URI is on the users website, it will authenticate the user and the action therefore will happen on the users site and send an [ActivityPush](http://activitypush.org/) to the thrid-party website about it. This is kinda like a bookmarklet to a URI on your website that is automatically invoked by a third-party website.

* This could also be implemented as a bookmarklet that parses a microformats on the resource it is invoked on and presents all possible actions allowed on that resource. Browsers should eventually implement this.


## See also
* [Web Actions](http://waterpigs.co.uk/articles/web-actions) by Barnaby Walters
* [Web Intents](http://webintents.org/)
* [Web Actions: Identifying A New Building Block For The Web](http://tantek.com/2011/220/b1/web-actions-a-new-building-block) by Tantek