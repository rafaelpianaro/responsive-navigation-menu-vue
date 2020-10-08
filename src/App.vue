<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/> -->
  <div id="app">
    <ResponsiveNavigation 
      :nav-links="navLinks"
    />
    <router-view/>
  </div>
</template>

<script>

import ResponsiveNavigation from '@/components/ResponsiveNavigation'
export default {
  data(){
    return {
      navLinks: [
      {
        text: 'Contact',
        path: '/contact',
        icon: 'ion-ios-megaphone'
          },
          {
            text: 'About',
        path: '/about',
        icon: 'ion-ios-business'
          },
          {
            text: 'Blog',
        path: '/blog',
        icon: 'ion-ios-bonfire'
          },
          {
            text: 'Portfolio',
        path: '/portfolio',
        icon: 'ion-ios-briefcase'
          }
        ]
    }
  },
  components: {
    ResponsiveNavigation
  }
}
</script>


<style lang='scss'>
@import 'https://unpkg.com/ionicons@4.2.2/dist/css/ionicons.min.css';
figure {
	margin-block-start: 0;
	margin-block-end: 0;
	margin-inline-start: 10px;
	margin-inline-end: 0;
}
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
