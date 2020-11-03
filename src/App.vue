<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/show">User Resume</router-link> |
      <router-link to="/login">Login</router-link> |
      <router-link to="/logout">Logout</router-link> |
      <router-link to="/signup">Signup</router-link> |
    </div>
    <router-view />
  </div>
</template>

<style>

  body {
  font-family: Futura, "Trebuchet MS", Arial, sans-serif;
  background-image: url("./assets/double-bubble.png");
  }

</style>
