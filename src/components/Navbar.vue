<template>
  <mdb-navbar color="elegant-color" dark class="code">
    <mdb-navbar-brand>
      <span>Nickert</span>
      <code class="pink-text">.dev</code>
    </mdb-navbar-brand>
    <mdb-navbar-toggler>
      <mdb-navbar-nav right>
        <!-- <router-link to="/about">
          <mdb-nav-item>About</mdb-nav-item>
        </router-link>
        <router-link to="/about">
          <mdb-nav-item>About</mdb-nav-item>
        </router-link> -->
        <a href="https://www.linkedin.com/in/cameron-nickert/" target="_blank">
          <mdb-nav-item class="p-0">
            <i class="fa fab fa-linkedin" style="font-size: 1.1rem;"></i>
          </mdb-nav-item>
        </a>
      </mdb-navbar-nav>
      <!-- <form>
        <mdb-input
          type="text"
          class="text-white"
          placeholder="Search"
          aria-label="Search"
          label
          navInput
          waves
          waves-fixed
        />
      </form>-->
    </mdb-navbar-toggler>
  </mdb-navbar>
</template>

<script>
import {
  mdbNavbar,
  mdbNavbarBrand,
  mdbNavbarToggler,
  mdbNavbarNav,
  mdbNavItem
} from "mdbvue";
export default {
  name: "Navbar",
  components: {
    mdbNavbar,
    mdbNavbarBrand,
    mdbNavbarToggler,
    mdbNavbarNav,
    mdbNavItem
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.navbar-brand {
  font-family: "Courier Prime Code";
}
</style>
