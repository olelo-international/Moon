---
layout: page
title: Developer Guide
tags: [walkthrough, meteor, galaxy, olelo]
date: 2018-04-24
comments: false
---
    
<h2>Installation</h2>

First, **install [Meteor](https://www.meteor.com/install)**.

Second, **download a copy of ʻŌlelo International**.

Third, cd into the app directory install the required libraries with:

      $ meteor npm install

Once the libraries are installed, you can run the application by invoking:

      $ meteor npm run start

The first time you run the app, it will create some default users and data. Here is the output:

      > meteor-application-template-react@ start /Users/sabinestrasburger/Desktop/GitHub/meteor-application-template-react/app
      > meteor --no-release-check --settings ../config/settings.development.json
      
      [[[[[ ~/Desktop/GitHub/meteor-application-template-react/app ]]]]]
      
      => Started proxy.                             
      => Started MongoDB. 
      I20180305-18:06:02.764(-10)? Creating the default user(s)
      I20180305-18:06:02.803(-10)?   Creating user admin@foo.com.
      I20180305-18:06:02.803(-10)?   Creating user john@foo.com.
      I20180305-18:06:02.804(-10)? Creating default contacts.
      I20180305-18:06:02.804(-10)?   Adding: Johnson (john@foo.com)
      I20180305-18:06:02.804(-10)?   Adding: Casanova (john@foo.com)
      I20180305-18:06:02.804(-10)?   Adding: Binsted (admin@foo.com)                          
      => Started your app.                          
      
      => App running at: http://localhost:3000/
      W20180322-08:57:42.354(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
      W20180322-08:57:42.423(-10)? (STDERR) While this implementation will work correctly, it is known to be
      W20180322-08:57:42.423(-10)? (STDERR) approximately three times slower than the native implementation.
      W20180322-08:57:42.424(-10)? (STDERR) In order to use the native implementation instead, run
      W20180322-08:57:42.424(-10)? (STDERR) 
      W20180322-08:57:42.425(-10)? (STDERR)   meteor npm install --save bcrypt
      W20180322-08:57:42.425(-10)? (STDERR) 
      W20180322-08:57:42.425(-10)? (STDERR) in the root directory of your application.

**Note regarding bcrypt warning.** You will also get the following message when you run this application:

      Note: you are using a pure-JavaScript implementation of bcrypt.
      While this implementation will work correctly, it is known to be
      approximately three times slower than the native implementation.
      In order to use the native implementation instead, run
      
        meteor npm install --save bcrypt
      
      in the root directory of your application.

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

If all goes well, the template application will appear at http://localhost:3000. You can login using the credentials in settings.development.json, or else register a new account.

Lastly, you can run ESLint over the code in the imports/ directory with:

      meteor npm run lint
