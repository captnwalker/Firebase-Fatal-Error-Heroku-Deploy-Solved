# Firebase/Heroku Fatal Deploy Error Solved   :four::zero::four:

## FIREBASE FATAL ERROR: Can't determine Firebase Database URL

## Purpose of this Repo

>This documentation seeks to provide one possible solution to a specific error that may be encountered when deploying an app utilizing FirebaseDB/AuthO to Heroku. If you have insights or other possible solutions, please open an issue.

### Error Output from Chrome Developers Console

`util.js:220 Uncaught Error: FIREBASE FATAL ERROR: Can't determine Firebase Database URL.  Be sure to include databaseURL option when calling firebase.intializeApp().
    at t.fatal (https://your-site.herokuapp.com/dist/bundle.js:7:2745)
    at e.databaseFromApp (https://your-site.herokuapp.com/dist/bundle.js:123:505)
    at Object.t.INTERNAL.registerService.Reference [as database] (https://your-site.herokuapp.com/dist/bundle.js:276:147519)
    at e._getService (https://your-site.herokuapp.com/dist/bundle.js:273:1493)
    at e.f.(anonymous function) [as database] (https://your-site.herokuapp.com/dist/bundle.js:270:1493)
    at Object.s [as database] (https://your-site.herokuapp.com/dist/bundle.js:270:1320)
    at Object.<anonymous> (https://your-site.herokuapp.com/dist/bundle.js:99:43448)
    at t (https://your-site.herokuapp.com/dist/bundle.js:1:101)
    at Object.<anonymous> (https://your-site.herokuapp.com/dist/bundle.js:99:41641)
    at t (https://your-site.herokuapp.com/dist/bundle.js:1:101)`

### What Occurred

>App built in React/Redux/Webpack/Firebase DB and Authentication. App is authenticating, CRUD’ing data to Firebase DB and functioning properly on localhost. After successful deploy and build of site to Heroku, the above error is received in Google Chrome Developers Console. Error was replicated on more than 3 attempts to deploy different apps.

### How to Repair

1. Insure that you have set your Firebase API keys in Heroku from the command line: `heroku config:set <list all 6 keys copied from your .env file and separated by a space>`
2. Redeploy to Heroku so that site recompiles and successfully connects to Firebase.

---

#### Initially Posted 3/3/2018

#### License -  MIT

#### Author

* **Steve Walker**  | [LinkedIn](https://www.linkedin.com/in/stevelwalker/)