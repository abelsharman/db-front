<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/login">Login</router-link> |
      <router-link to="/register">Register</router-link> |
      <router-link to="/cab">Cab</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
#nav{
  width: 100vw;
  height: 60px;
  background-color: black;
  opacity: 0.3;
  position: relative;
  z-index: 100000;
  text-align: center;
  color: white;
  font-size: 2vw;
  padding-top: 10px
}
#nav a{
  text-align: center;
  text-decoration: none;
  color: white;
}
</style>
