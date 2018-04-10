# Firebase-For-Web

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

## 1) Firebase Realtime Database 
### 1.1) Write Operation

```js

<script>
  var name="Name";
  
  // Overwite the Data
  firebase.database().ref('data').set({name:name});
  
  // Append the Data and create unique key
  firebase.database().ref('data').push({name:name});
  
</script>

```

### 1.2) Read Operation

```js

<script>
  var name="Name";

  firebase.database().ref('data').one('value',(snap)=>{
    console.log(snap.val());
  });

</script>

```


## 2) Firebase Authentication  
### 1.2) Auth with Email and Password
#### 1.2.1) Sign Up New User
Create a form that allows new users to register with your app using their email address and a password. When a user completes the form, validate the email address and password provided by the user, then pass them to the `createUserWithEmailAndPassword` method:
```js


<script>
 
  var email="someone@example.com";
  var password="password";
  
  //Create User with Email and Password
  firebase.auth().createUserWithEmailAndPassword(email, password).catch(function(error) {
    // Handle Errors here.
    var errorCode = error.code;
    var errorMessage = error.message;
    console.log(errorCode);
    console.log(errorMessage);
  });
  
</script>

```


#### 1.2.2) Sign In User
Create a form that allows existing users to sign in using their email address and password. When a user completes the form, call the `signInWithEmailAndPassword` method:


```js
<script>
  
  var email="someone@example.com";
  var password="password";
  
  //Sign In User with Email and Password
  firebase.auth().signInWithEmailAndPassword(email, password).catch(function(error) {
    // Handle Errors here.
    var errorCode = error.code;
    var errorMessage = error.message;
    console.log(errorCode);
    console.log(errorMessage);
});

  
</script>

```

#### 1.2.3) Set an authentication state observer and get user data

For each of your app's pages that need information about the signed-in user, attach an observer to the global authentication object. This observer gets called whenever the user's sign-in state changes.

Attach the observer using the `onAuthStateChanged` method. When a user successfully signs in, you can get information about the user in the observer.


```js

firebase.auth().onAuthStateChanged(function(user) {
  if (user) {
    // User is signed in.
    var displayName = user.displayName;
    var email = user.email;
    var emailVerified = user.emailVerified;
    var photoURL = user.photoURL;
    var isAnonymous = user.isAnonymous;
    var uid = user.uid;
    var providerData = user.providerData;
    // ...
  } else {
    // User is signed out.
    // ...
  }
});

```

#### 1.2.4) Sign Out User

To sign out a user, call `signOut`:

```js
firebase.auth().signOut().then(function() {
  // Sign-out successful.
  console.log('User Logged Out!');
}).catch(function(error) {
  // An error happened.
  console.log(error);
});
```




