<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/databindingradio">Data Binding</router-link> |
    <router-link to="/DataBindingAtrribue">Data Atrribue</router-link> |
    <router-link to="/DataBindingButton">Data Button</router-link> |
    <router-link to="/DataBindingClass">Data Class</router-link> |
    <router-link to="/DataBindingList">Data List</router-link> |
    <router-link to="/DataBindingList2">Data List2</router-link> |
    <router-link to="/NestedComponent">Nested</router-link> |
  </nav>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
