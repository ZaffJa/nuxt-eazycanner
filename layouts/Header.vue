<template>
  <div class="container-fluid p-0">
    <div class="col-xs-12 w-100 text-white bg-main">
      <span class="pl-4" />
      <fai icon="envelope" style="height: 17px; width: 17px;" />
      <span>+018-870 2422</span>
      <fai icon="phone" style="height: 17px; width: 17px; margin-left: 10px;" />
      <span>rahman@eazycanner.com</span>
    </div>
    <div class="nav">
      <div class="nav-header">
        <img src="~assets/images/black.png" style="margin: 13px; display: inline-block;" alt="logo">
      </div>
      <div class="nav-btn" @click="toggle()">
        <label for="nav-check">
          <span />
          <span />
          <span />
        </label>
      </div>
      <input id="nav-check" type="checkbox">
      <div class="nav-links position-absolute" style="right: 0px;" :class="[isToggled ? 'show-dropdown': 'hide-dropdown']" @click="toggle()">
        <nuxt-link to="/">
          Home
        </nuxt-link>
        <nuxt-link to="/about">
          About Us
        </nuxt-link>
        <nuxt-link to="/how-to-buy">
          How To Buy
        </nuxt-link>
        <nuxt-link to="/contact-us">
          Contact Us
        </nuxt-link>
        <nuxt-link to="/additional-details">
          Additional Details
        </nuxt-link>
        <nuxt-link to="/donation">
          Donation
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isToggled: false
    }
  },
  methods: {
    toggle() {
      this.isToggled = !this.isToggled
    }
  }
}
</script>


<style>
.nav {
  height: 70px;
  width: 100%;
  position: relative;
  -webkit-box-shadow: 0px 5px 17px -6px rgba(0, 0, 0, 0.5);
  -moz-box-shadow: 0px 5px 17px -6px rgba(0, 0, 0, 0.5);
  box-shadow: 0px 5px 17px -6px rgba(0, 0, 0, 0.5);
}

.nav > .nav-header {
  display: inline;
}

.nav > .nav-btn {
  display: none;
}

.nav > .nav-links {
  display: inline;
  font-size: 18px;
}

.nav > .nav-links > a {
  display: inline-block;
  padding: 20px 15px;
  color: black;
  text-decoration: none;
}

.nav > .nav-links > a:hover {
  color: #10b8d2;
}

.nav > #nav-check {
  display: none;
}

@media (max-width: 1000px) {
  .nav > .nav-btn {
    display: inline-block;
    position: absolute;
    right: 0px;
    top: 0px;
  }
  .nav > .nav-btn > label {
    display: inline-block;
    width: 50px;
    height: 50px;
    padding: 20px;
    cursor: pointer;
    margin-right: 20px;
  }
  .nav > .nav-btn > label > span {
    display: block;
    width: 25px;
    height: 10px;
    border-top: 2px solid #eee;
  }
  .nav > .nav-links {
    position: absolute;
    display: block;
    width: 100%;
    background-color: whitesmoke;
    transition: all 0.3s ease-in;
    overflow-y: hidden;
    top: 70px;
    left: 0px;
    z-index: 9999;
  }
  .nav > .nav-links > a {
    display: block;
    width: 100%;
  }
  /* .nav > #nav-check:not(:checked) + .nav-links {
    height: 0px;
  } */
  /* .nav > #nav-check:checked + .nav-links {
    height: calc(80vh - 50px);
    overflow-y: auto;
  } */
}

.show-dropdown {
  height: calc(80vh - 50px);
  overflow-y: auto;
}

.hide-dropdown {
  height: 0px;
}
</style>
