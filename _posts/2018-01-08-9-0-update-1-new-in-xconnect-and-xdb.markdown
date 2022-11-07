---
layout: post
title: "9.0 Update-1: New in xConnect and xDB"
date: 2018-08-01
categories: tech
permalink: /2018/01/08/9-0-update-1-new-in-xconnect-and-xdb/
---

Here are some of the key changes made to xConnect and the xDB in the recently released [9.0 Update 1](https://dev.sitecore.net/Downloads/Sitecore_Experience_Platform/90/Sitecore_Experience_Platform_90_Update1.aspx) -- including links to documentation. For a full list of changes, see the official [release notes](https://dev.sitecore.net/Downloads/Sitecore%20Experience%20Platform/90/Sitecore%20Experience%20Platform%2090%20Update1/Release%20Notes).

xDB.Tracker identifier available as a constant
----------------------------------------------

Any contact that visits your website is given a [tracker identifier](http://doc.sitecore.net/developers/xp/xconnect/xconnect-model/contacts/contact-identifiers.html#tracker-identifier). The identifier is a GUID (the same GUID represented by\
`Sitecore.Analytics.Tracker.Current.Contact.ContactId`) and the identifier source is "xDB.Tracker". In 9.0.1, the identifier source is available as a constant: `Sitecore.Analytics.XConnect.DataAccess.Constants.IdentifierSource`. This means that you can retrieve a contact by his or her tracker identifier without hard-coding the source.

Trigger interaction outcomes with custom data from tracker
----------------------------------------------------------

In the context of the tracker, you can [trigger an outcome for a particular page or for the entire interaction](http://doc.sitecore.net/developers/xp/tracking-and-session/tracker/tracking-events/trigger-built-in-event-types.html#trigger-an-outcome). In 9.0.0, you could trigger a page-level outcome with custom data. In 9.0.1, you can [include custom data for outcomes triggered at an interaction level as well](http://doc.sitecore.net/developers/xp/tracking-and-session/tracker/tracking-events/trigger-custom-event/index.html#capturing-custom-outcome-data).

Reload contact from xConnect after setting facets
-------------------------------------------------

In 9.0.1, the `RemoveFromSession()` method on the `ContactManager` class has made public. This method [reloads a contact from xConnect into shared session state](http://the http://doc.sitecore.net/developers/xp/tracking-and-session/tracker/tracking-contacts/contact-facets/update-facets.html#re-loading-contact-data), and can be used to refresh the facet values available in session after submitting changes to xConnect.

Note: If you do not reload the contact after submitting changes to xConnect -- such as updating their birth date or e-mail address -- the facet data that is being held in session will be out of date. In 9.0.0, you must manually updated the facet values held in session after submitting a change to xConnect.

Use custom facets in your custom activity types
-----------------------------------------------

Custom facets are now supported in [custom activity types](https://doc.sitecore.net/developers/xp/marketing-automation/activities/activity-types/create-an-activity-type.html).

Automation pool worker configuration
------------------------------------

Automation pool workers are now [added to the engine automatically](https://doc.sitecore.net/developers/xp/marketing-automation/automation-engine/processing/index.html#configure-pool-workers), although you can still configure the pool workers individually. You can also configure the number of times a work item will be retried before it will be [stalled](https://doc.sitecore.net/developers/xp/marketing-automation/automation-engine/processing/index.html#stalling-work-items).