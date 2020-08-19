<template>
  <header
    class="header"
    :class="{
      sticky: $route.path === '/' || $route.path.includes('/projects/'),
    }"
  >
    <div class="container">
      <div class="left">
        <g-link :to="{ name: 'home' }" class="home-link">
          <img
            src="../../static/miserable.png"
            :alt="settings.site_name"
            class="logo"
          />
        </g-link>
      </div>
      <span class="open-nav" @click="openMobileNav">Menu</span>
      <nav class="nav right" v-bind:class="{ isOpen: openNav }">
        <span class="close-nav" @click="openMobileNav">X</span>
        <g-link class="nav__link" to="/about">About Us</g-link>
        <!-- <g-link class="nav__link" to="/blog">Blog</g-link> -->
        <g-link class="nav__link" to="/contact">Say Hi!</g-link>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      logo: require('../../static/logo.svg'),
      settings: require('../../data/theme.json'),
      openNav: false
    };
  },
  methods: {
      openMobileNav() {
          console.log('hey')
          this.openNav = !this.openNav;
      }
  }
};
</script>

<style scoped lang="scss">
.header {
  position: relative;
  height: 6rem;
  z-index: 10;
}
.header.sticky {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
.header > .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
}
.home-link {
  text-decoration: none;
}
.logo {
  height: 1.5rem;
}
.site-name {
  font-size: 0.9rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-decoration: none;
  text-transform: uppercase;
}
.nav > * {
  font-size: 0.9rem;
  font-weight: 600;
  text-decoration: none;
  margin-top: 4px;
  margin-right: 3rem;
  padding-bottom: 4px;
  border-bottom: 1px solid;
  border-color: transparent;
  transition: border 0.15s;
}
.nav > *:last-of-type {
  margin: 0;
}
.nav > *:hover {
  border-color: inherit;
}
.nav > .active {
  border-color: inherit;
}
.right {
  @media only screen and (max-width: 550px) {
    display: none;
    position: absolute;
    background: black;
    width: 100%;
    top: 0;
    right: 0;
    padding-top: 3rem;
    padding-bottom: 3rem;
    padding-left: 2rem;
    .nav__link {
      color: white;
    }
  }
}
.close-nav {
  color: white;
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-size: 1.25rem;
  cursor: pointer;
}
.open-nav {
    font-weight: bold;
    cursor: pointer;
    display: none;
    @media only screen and (max-width: 550px) {
        display: block;
    }
}
.isOpen {
    display: block !important;
}
</style>
