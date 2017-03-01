# decision-maker

A web app that helps groups of friends to vote on a preferred choice (using ranked voting), for example: "What movie should we see next Friday?".

###Requirements:

- a user can create a poll with multiple choices
- each choice can have a title and optional description
- the creator must enter an email
- when a poll is finished being created, the user is given two links: an administrative link (which lets them access the results) and a submission link (which the user sends to their friends)
- the links are also sent to the creator via email (using mailgun)
- when a user visits the submission link, they enter their name if required (see extensions) and see a list of the choices for that poll
- the user can rank the choices (by drag and drop, or some other method) and then submits the poll
- each time a submission is received, the creator is notified with an email (which includes the administrative link and a link to the results)
- the results are ranked using the Borda Count method: https://en.wikipedia.org/wiki/Borda_count
- note: this app does not follow the typical user authentication process: voters don't need to register or log in and the only way to access the polls or see the results is via links

###Extensions:

- use the Instant Runoff algorithm instead of Borda Count: https://en.wikipedia.org/wiki/Instant-runoff_voting
- make the app work well on mobile
- allow the creator to enter their friends' emails when creating the poll and send the poll to those emails (using mailgun)
- allow the creator to enter phone numbers and send the poll link to those numbers (using twilio)
- make it so that the entire poll can be completed via SMS
- support uploading photos for choices (for example, to answer "which of these logos is best")
- let users put links as choices and use embed.ly to embed the content (would work well for map links)
- add unit tests (using mocha + chai)
- add end-to-end tests (using phantomjs)
- creator is given the option to require voters to enter a name (or not)

###Stack Requirements
Your projects must use:

- ES6 for server-side (Node) code
- ES5 for front-end code
- Node
- Express
  - RESTful routes
  - Using AJAX or complete SPA approach is optional
- One of the following two CSS grid and UI frameworks
  - Bootstrap 3
  - Zurb Foundation 5
- jQuery
- SASS for styling
- PostgreSQL for DB
- Knex.js for querying and migrations
- git for version control
- heroku for hosting (hosting is optional)

![erd](http://adriandgr.github.io/decision-maker/img/ERD.gif)

## Creating a poll mock-up
![mockups](http://adriandgr.github.io/decision-maker/img/mockups-spread.jpg)

