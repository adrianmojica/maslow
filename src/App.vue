<template>
  <div id="app">
    <div id="nav">
      <div class="bar">
        <img class="logo" src="./assets/logoh.png"/>
        <ul>
          <li><router-link to="/">Exercise</router-link></li>
          <li><router-link to="/about">About</router-link></li>
        </ul>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
body {
  margin:0px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.vue-slider {
  height: 12px !important;
}
.bar {
  background: #0053ee;
  height:60px;
  width:100%;
  ul {
    padding: 0px;
    margin: 0px;
    text-align: center;
    display:inline-block;
    vertical-align:top;
    li {
      list-style-type: none;
      padding: 0px;
      height: 24px;
      margin-top: 4px;
      margin-bottom: 4px;
      display: inline;
      a {
        color: white;
        font-size: 16px;
        font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
        text-decoration: none;
        line-height: 70px;
        padding: 5px 15px;
        opacity: 0.7;
      }
    }
  }
  .logo {
      width: 35px;
      float: left;
      margin-top:10px;
      margin-left:20px;
  }
}
#nav {
  a {
    font-weight: bold;
    color: white;

    &.router-link-exact-active {
      color: white;
      opacity: 1;
    }
  }
}
</style>
