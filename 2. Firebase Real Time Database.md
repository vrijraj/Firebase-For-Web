
## Firebase Realtime Database 
All Firebase Realtime Database data is stored as JSON objects. You can think of the database as a cloud-hosted JSON tree. Unlike a SQL database, there are no tables or records. When you add data to the JSON tree, it becomes a node in the existing JSON structure with an associated key. You can provide your own keys, such as user IDs or semantic names, or they can be provided for you using push().

### Write Operation

```js

<script>
  var name="Name";
  
  // Overwite the Data
  firebase.database().ref('data').set({name:name});
  
  // Append the Data and create unique key
  firebase.database().ref('data').push({name:name});
  
</script>

```

### Read Operation

```js

<script>

  firebase.database().ref('data').on('value',(snap)=>{
    console.log(snap.val());
  });

</script>

```
### Read List of Data

```js
<script>

  firebase.database().ref('ReferernceName').once('value', function(snapshot) {
    snapshot.forEach(function(childSnapshot) {
      var childKey = childSnapshot.key;
      var childData = childSnapshot.val();
      // ...
    });
  });
  
</script>
```

### Count the Number of Nodes

```js

<script>

  firebase.database().ref('data').on('value',(snap)=>{
    var totalRecord =  snap.numChildren();
    console.log("Total Record : "+totalRecord);
  });

</script>

```

### Delete Operation

The simplest way to delete data is to call `remove()` on a reference to the location of that data.

You can also delete by specifying null as the value for another write operation such as `set()` or `update()`. You can use this technique with `update()` to delete multiple children in a single API call.
