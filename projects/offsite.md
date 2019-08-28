---
layout: default
permalink: projects/offsite
---

# OffSite

I'm a Core engineer for OffSite, a venture backed digital marketing app (**[Marketing Website](https://connectoffsite.com/)**).

OffSite is a fairly complex Rails application with React components embedded throughout. It offers a set of features on top of Google Ads (Google Ads API) that allows parties to share Google Ads audiences without disclosing a user’s personally identifiable information.

OffSite has relatively few traditional models, but incorporates a number of classes that behave like ActiveRecord Models (and include ActiveModel::Model) while persisting data on Google Ads rather than in the database. Many seemingly simple interactions in OffSite also include loading Google OAuth credentials for multiple parties to take API-level actions on the user’s behalf.

Some features I personally worked on:

* Initial OffSite onboarding flow for new users and created an invitation system for current users to invite new users to their team on OffSite
* Elaborate ActiveJob that could pull a user's existing Google Ad's campaigns and ads and import them onto OffSite to be used
* Tasks that pull data from Google Ads API and updates user data in our database when necessary on the user’s behalf

Some features in Offsite require an admin to step in and manually complete some processes in a "manager account" in Google Ads. We use state machines (AASM gem) and ActiveJob to pull these changes from user’s Google Ads Accounts and update their records in our database.

_Google Ads API, Devise, Honey Badger, Stripe, AASM state machines, Simple Form, Activity Notification, Sidkiq, Simple Scheduler, VCR_


## Screenshots

* * *

![Me](/assets/images/offsite-login.png)

* * *

#### Owner Onboarding: Audience Owner Profile Form
This form is created using React and Formik

* * *

![Me](/assets/images/offsite-owner-profile.png)

* * *

#### Owner Onboarding: Owner Selects Which of their Audiences to Import to Offsite
This form is created using React and Formik

* * *

![Me](/assets/images/owner-audience-select.png)

* * *

#### Onboarding: Owner Edits Audience Information While Importing To Offsite
This form is created using React and Formik and is showing validation errors through Yup

* * *

![Me](/assets/images/offsite-audience-profile.png)

* * *

#### Owner Invitation System

* * *
![Me](/assets/images/offsite-invitation.png)
