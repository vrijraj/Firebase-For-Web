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

var name1 = $.request.parameters.get('name');
var conn = $.db.getConnection(); 
var pstmt = conn.prepareStatement( "INSERT INTO ADMIN.USER_DATA VALUES(?)" );
pstmt.setString(1,name1);
pstmt.execute(); 
conn.commit(); 
$.response.contentType = 'text/plain';
$.response.setBody('Data Inserted');
$.response.status = 200;

```

