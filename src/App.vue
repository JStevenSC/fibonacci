<template>
  <div>
    <nav>
      <router-link to="/">Hitoria</router-link> |
      <router-link to="/about">Reloj</router-link>
    </nav>
    <router-view/>

    <footer>
      <p>Juan Steven Sanchez Castro</p>
    </footer>
  </div>

</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  background-color: #816474a2;

  background-image: linear-gradient(to left,rgb(3, 63, 71),rgb(6, 113, 128));

  a {
    font-weight: bold;
    color: #ffffff;

    &.router-link-exact-active {
      color: #d0cdf1;
    }
  }
}

footer {
  padding: 20px;
  color: #ffffff;

  background-image: linear-gradient(to left,rgb(3, 63, 71),rgb(6, 113, 128));

  a {
    font-weight: bold;
    color: #ffffff;

    &.router-link-exact-active {
      color: #d0cdf1;
    }
  }
}
</style>
