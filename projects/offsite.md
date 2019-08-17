---
layout: default
permalink: projects/offsite
---

# OffSite

I'm a Core engineer for OffSite, a venture backed digital marketing app (**[Marketing Website](https://connectoffsite.com/)**).

OffSite is a fairly complex Rails application with React components embedded throughout. It offers a set of features on top of Google Ads that allows parties to share Google Ads audiences without disclosing a user’s personally identifiable information.

OffSite has relatively few traditional models, but incorporates a number of classes that behave like ActiveRecord Models (and include ActiveModel::Model) while persisting data on Google Ads rather than in the database. Many seemingly simple interactions in OffSite also include loading Google OAuth credentials for multiple parties to take API-level actions on the user’s behalf.

Some features I personally worked on:

* Built the initial OffSite onboarding flow for new users and created an invitation system for current users to invite new users to their team on OffSite
* Implemented an elaborate ActiveJob that could pull a user's existing Google Ad's campaigns and ads and import them onto OffSite to be used
* Created tasks that pull data from Google Ads API and updates user data in our database when necessary on the user’s behalf

Some features in Offsite require an admin to step in and manually complete some processes in a "manager account" in Google Ads. We use state machines (AASM gem) and ActiveJob to pull these changes from user’s Google Ads Accounts and update their records in our database.

_Google Ads API, Devise, Honey Badger, Stripe, AASM state machines, Simple Form, Activity Notification, Sidkiq, Simple Scheduler, VCR_
