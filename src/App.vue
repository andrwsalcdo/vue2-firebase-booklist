<template>
  <div id="app">

  </div>
</template>

<script>
import Hello from './components/Hello'

import Firebase from 'firebase'

let config = {
  apiKey: "AIzaSyDQuyPKOe6U7zTtey2pTaucEad3DYg03ZI",
  authDomain: "vue2-firebase-booklist.firebaseapp.com",
  databaseURL: "https://vue2-firebase-booklist.firebaseio.com",
  storageBucket: "vue2-firebase-booklist.appspot.com",
  messagingSenderId: "212113090399"
}

let app = Firebase.initializeApp(config);
let db = app.database();

let booksRef = db.ref('books');

export default {
  name: 'app',
  firebase: {
    books: booksRef
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
