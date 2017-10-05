# FDA-WebApp
Documentation for Development of mapping web portal for FDA inspection data.

Recreate functionality in Legacy's app: http://gis.truthinitiative.org/tobaccoviewer/   
From the Truth Initiative Tobacco Viewer About section:  

> This application was developed as a tool that allows for the examination of changes in FDA compliance check inspections over time. The tool is integrated with Truth Initiative’s GIS portal, which allows users to explore how compliance check inspections may be associated with a range of other factors. Users can quickly zoom to their local area and bookmark their preferences as they overlay various data sources and visualize the results.

### Phase 1:  User Stores and Tech Overview

User stories are described in Jira, the Tech Overview should be written in the README file of the github repo for this project.  This file (and all files, actually) should be committed and pushed to the repo every few hours during development.

**User Stories:**

We should pretend that the Legacy site is going away, and that we need to write down explicitly a User Stores that describes what the web app does (or what we are proposing it does.)  In other words, we can't simply say "Replicate the functionality of the Legacy website"), but rather describe in explicit detail what's expected, e.g.

"The user will be  able to click on a "Search Inspections" button that prompts the user for a date range and inspection type form.  Clicking on the Search button will list the search results and display them on the map".  Andrew's app has a range of other features too, like the ability to click on individual retailer points and click a link that brings up corresponding documents related to the outlet's inspection history.

This should be relatively easy to do, since it's simply running the current website and describing that it already does.  Of course, we could add more things at this point, but this step is absolutely critical.  We have to describe, in User Stories, exactly WHAT we want the app to do and agree on it before breaking this down into Tasks that describe HOW we're going to do it.  

**Technical Proposal:**

A one or two page overview that includes all the relevant technologies and basic timeline/sequence.  This should list specific technologies for each major component within the system.  It shouldn't simply be a list (e.g. "We're going to use PostGIS and Python"), but rather a breakdown for each individual component ("The import script be run from the command line and written in Python, and will store data on a PostGIS RDS instance.")

### Phase 2: Development/Coding

Once the Technical Proposal and User Stories have been agreed upon, the User Stories will be broken down into tasks that take between 1 and 4 hours to complete.  Every github commit MUST reference a Jira Task.  And github commits should take place frequently, every hour or so.

In the spirit of scrum, the code should also be pushed to a website, so that every day progress on the app can be seen.  It might start of with a simple list or CartoDb map, and then each day as tools are added we'll be able to see and test them.
