<template>
  <div class="linkedin-box text-left">
    <div
      class="LI-profile-badge"
      data-version="v1"
      data-size="large"
      data-locale="en_US"
      data-type="horizontal"
      data-theme="light"
      data-vanity="cameron-nickert"
    >
      <a
        class="LI-simple-link"
        href="https://www.linkedin.com/in/cameron-nickert?trk=profile-badge"
      >Cameron Nickert</a>
    </div>
  </div>
</template>

<script>
//import "./Profile.js";

export default {
  name: "LinkedInBox",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
