<template>
  <div id="app" :class="{ 'no-padding': route.path === '/try' }">
    <nav v-if="route.path !== '/try'" class="main-nav">
      <div class="container nav-container">
        <router-link to="/" class="nav-logo">SAM 2</router-link>
        <div class="nav-links">
          <router-link to="/">Home</router-link>
          <router-link to="/try">Try Demo</router-link>
          <router-link to="/about">About</router-link>
          <router-link to="/contact">Contact</router-link>
        </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
const route = useRoute()
</script>

<style>
html, body {
  width: 100%;
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}
#app {
  min-height: 100vh;
  width: 100%;
  box-sizing: border-box;
  /* background: #111; */
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding-top: 72px;
}
#app.no-padding {
  padding-top: 0;
}

.main-nav {
  background: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 0;
  max-width: 1200px;
  margin: 0 auto;
}

.nav-logo {
  font-size: 1.5em;
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 24px;
}

.nav-links a {
  color: #2c3e50;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #42b883;
}

.nav-links a.router-link-active {
  color: #42b883;
}
</style>
