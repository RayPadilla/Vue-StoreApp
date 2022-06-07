<template>
  <div class="navbar">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/store">Store</router-link> |
      <router-link to="/cart">Cart</router-link>
    </nav>
  </div>
  <router-view />
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0px;
  background-color: #cfdee7;
}

.navbar {
  background-color: #647aa3;
  box-shadow: 0 2px 2px 2px rgba(0, 0, 0, 0.25);
}

nav {
  padding: 20px;
  text-align: left;
  color: white;

  a {
    font-weight: bold;
    color: white;
    padding: 15px;

    &.router-link-exact-active {
      color: #334195;
    }
  }
}
</style>
