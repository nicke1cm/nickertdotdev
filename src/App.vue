<template>
  <div id="app">
    <div id="nav">
      <Navbar />
    </div>
    <router-view />
  </div>
</template>

<script>
import Navbar from "./components/Navbar";

export default {
  name: "App",
  components: {
    Navbar
  }
};
</script>

<style lang="scss">
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import "~@fortawesome/fontawesome-free/css/brands.min.css";
@import "~bootstrap-css-only/css/bootstrap.min.css";
@import "~mdbvue/lib/css/mdb.min.css";
@import url("https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap");

@font-face {
  font-family: "Courier Prime Code";
  src: url(./fonts/Courier-Prime-Code.ttf);
  font-weight: normal;
}

#app {
  font-family: "Roboto", Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

html, body {
  height: 100%;
}

code, .code {
  font-family: "Courier Prime Code";
}
</style>
