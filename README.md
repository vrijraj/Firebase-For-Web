# Firebase-For-Web Tutorials


Welcome Folks, Here you can find Firebase for Web Tutorial in easy language.

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

```js
var headers = new Headers();
headers.append('Content-Type', 'text/json');
headers.append('X-Custom-Header', 'SomeValue');

//We can achieve the same can by passing an object literal to the constructor

var headers = new Headers({
    'Content-Type': 'text/json',
    'X-Custom-Header': 'SomeValue'
});

```

