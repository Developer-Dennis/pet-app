<template>
  <nav>
    <router-link to="/">Home</router-link> 
    <router-link v-bind:to="{name: 'about'}">About</router-link>
  </nav>
  <router-view/>
</template>

<style>
body{
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #231f20;
  color: white;
  padding: 20px 50px;
}

nav a {
  font-size: 30px;
  text-decoration: none;
  color: white;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
