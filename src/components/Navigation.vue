<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
          Orchard Parent Portal
        </a>
        <a role="button" class="navbar-burger" @click="toggleMenu" :class="isMenuOpen ? 'is-active' : '' " aria-label="menu" aria-expanded="false">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
      </a>

      </div>
      <div class="navbar-menu" :class="isMenuOpen ? 'is-active' : ''">
        <div class="navbar-end" v-if="isSignedIn">
          <div class="navbar-item" :key="navItem.label" v-for="navItem in navItems">
            <router-link :to="navItem.link">{{ navItem.label }}</router-link>
          </div>
          <div class="navbar-item">
            <a @click="signOut" class="button is-primary">Log Out</a>
          </div>
        </div>
        <div class="navbar-end" v-else>
          <div class="navbar-item">
            <a @click="signIn" class="button is-primary">Log In</a>
          </div>
        </div>
      </div>
    </nav>
</template>

<script>

export default {
  name: 'Navigation',
  data: function () {
    return {
      isMenuOpen: false,
      isSignedIn: false,
      navItems: [{
        label: 'Home',
        link: '/'
      }, {
        label: 'Activities',
        link: '/activities'
      }, {
        label: 'Tasks',
        link: '/tasks'
      }, {
        label: 'Hours',
        link: '/hours'
      }
      ]
    }
  },
  methods: {
    toggleMenu: function () {
      this.isMenuOpen = !this.isMenuOpen
      console.log('toggleMenu - isMenuOpen: ' + this.isMenuOpen)
    },
    signIn: function () {
      this.isSignedIn = true
      this.$router.push('home')
    },
    signOut: function () {
      this.isSignedIn = false
      this.$router.push('signin')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
