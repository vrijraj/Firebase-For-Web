# Firebase Setup

Create a HTML page and include JS code from [Firebase Web Console](https://console.firebase.google.com)

Be sure to paste the configuration code into your web page as described.
```js
<script src="https://www.gstatic.com/firebasejs/4.12.1/firebase.js"></script>
<script>
  // Initialize Firebase
  var config = {
    apiKey: "xxxxxxxxxxxxxxxxxxxxxxx",
    authDomain: "xxxxxxxxxx.firebaseapp.com",
    databaseURL: "https://xxxxxxxxxxxxxx.firebaseio.com",
    projectId: "xxxxxxxxxxxxxxxxxxxxxxx",
    storageBucket: "xxxxxxxxxxxxxxxxxxxxxxx.appspot.com",
    messagingSenderId: "xxxxxxxxxxxxxxxxxxxxxxx"
  };
  firebase.initializeApp(config);
  
  // your code
  //...
  
  </script>

```

# Second Way! (If you are using Firebase Hosting)

#### Host your Web App Using Firebase Hosting

If you are building a web app and your web app is entirely static content, you can deploy it easily using Firebase Hosting.

Firebase Hosting is a developer-focused static web hosting for modern front-end web applications. Using Firebase Hosting, you can deploy SSL-enabled web apps to your own domain on a global content-delivery network (CDN) from a single command.

Web apps hosted with Firebase Hosting can benefit from simpler project configuration. Paste the following code snippets into your application HTML to import the Firebase SDK and configure it automatically for the project your app is hosted on:

```js

    <!-- Firebase App is always required and must be first -->
    <script src="/__/firebase/5.0.4/firebase-app.js"></script>

    <!-- Add additional services you want to use -->
    <script src="/__/firebase/5.0.4/firebase-auth.js"></script>
    <script src="/__/firebase/5.0.4/firebase-database.js"></script>
    <script src="/__/firebase/5.0.4/firebase-messaging.js"></script>
    <script src="/__/firebase/5.0.4/firebase-functions.js"></script>

    <!-- Comment out (or don't include) services you don't want to use -->
    <!-- <script src="/__/firebase/5.0.4/firebase-storage.js"></script> -->

    <script src="/__/firebase/init.js"></script>

```
