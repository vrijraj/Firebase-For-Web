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


```html
<!doctype html>
<html lang="en">
 <head>
 <title>Hello, world!</title>
 <! - Required meta tags →
 <meta charset="utf-8">
 <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<script>
 var a=window.location.hrefurl.searchParams.get('x');
 console.log(x);
</script>
 <! - Bootstrap CSS →
 <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" integrity="sha384-PsH8R72JQ3SOdhVi3uxftmaW6Vc51MKb0q5P2rRUpPvrszuE4W1povHYgTpBfshb" crossorigin="anonymous">
 </head>
 <body>
 <div class="container">
 <div class="row">
 <div class="col-md-12">
 <br>
 <br>
 <h2>SAP HANA CRUD</h2> 
 <hr>
 
 </div>
 </div>
 
 <div class="row">
 <div class="col-md-6">
 <form method="get" action="add.xsjs">
 <input type="text" class="form-control" placeholder="Enter email" name="name">
 <br>
 <button type="submit" class="btn btn-primary">Submit</button>
 </form> 
 </div>
 </div>
 </div>
<! - Optional JavaScript →
 <! - jQuery first, then Popper.js, then Bootstrap JS →
 <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
 <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.3/umd/popper.min.js" integrity="sha384-vFJXuSJphROIrBnz7yo7oB41mKfc8JzQZiCq4NCceLEaO4IHwicKwpJf9c9IpFgh" crossorigin="anonymous"></script>
 <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/js/bootstrap.min.js" integrity="sha384-alpBpkh1PFOepccYVYDB4do5UnbKysX5WZXm3XxPqe5iKTfUKjNkCk9SaVuEZflJ" crossorigin="anonymous"></script>
 </body>
</html>
```

