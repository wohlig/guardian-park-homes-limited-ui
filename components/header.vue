<template>
  <div class="container">
    <div class="header-section ">
      <div class="bg-white text-dark">
        <b-navbar toggleable="lg">
          <b-navbar-brand class="header-logo">
            <nuxt-link to="/">
              <img src="@/assets/images/logo.svg" alt="logo" />
            </nuxt-link>
          </b-navbar-brand>
          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
          <b-collapse
            id="nav-collapse"
            is-nav
            class="justify-content-center pt-3"
          >
            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto text-dark font-20 secondary">
              <b-nav-item href="#" class=" active">
                <nuxt-link to="/">Home</nuxt-link></b-nav-item
              >
               <b-nav-item href="#" class="">
                <nuxt-link to="/our-mobile-home">Our Mobile Home</nuxt-link></b-nav-item
              >
               <b-nav-item href="#" class="">
                <nuxt-link to="/design-collection">Design Collection </nuxt-link></b-nav-item
              >
              <b-nav-item href="#" class="">
                <nuxt-link to="/about-us">About Us</nuxt-link></b-nav-item
              >
              <b-nav-item href="#">
                <nuxt-link to="/contact-us">Contact Us</nuxt-link></b-nav-item
              >
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
@import "~assets/scss/_variable";
.navbar-toggler {
  background: $white;
  padding: 5px 10px;
  &:focus {
    outline: none;
  }
}
.navbar-light .navbar-toggler-icon {
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='30' height='30' viewBox='0 0 30 30'%3e%3cpath stroke='rgba%280, 0, 0, 01' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
}

.header-section {
  .header-logo {
    width: 120px;
    img {
      width: 100%;
    }
  }
  .navbar {
    padding: 10px 0px;
    .nuxt-link-exact-active.nuxt-link-active {
      color: $primary;
      font-weight: bold;
      text-decoration: none;
    }
    .nav-link {
      padding: 0px;
      a {
        color: $black;
        padding: 0 20px;
        text-decoration: none;
        font-weight: bold;
        &:hover {
          color: $primary;
          font-weight: bold;
        }
      }
    }
    .nav-item {
      text-align: center;
      border: none;
      padding-bottom: 15px;
      padding-top: 5px;
    }
  }
}
</style>
