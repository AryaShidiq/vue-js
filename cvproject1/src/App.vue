<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Footer1 from './components/Footer.vue';
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col-md p-3">
          <img alt="Personal photo" class="logo text-center m-auto d-block" src="@/assets/fotodiri.png" width="125" height="125" />
        </div>
        <div class="col-md p-3">
          <Navbar/>
        </div>
      </div>
    </div>
  </header>
  <main>
    
  </main>
  <!-- <Footer>
    <Footer1/>
  </Footer> -->
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  margin: 0 2rem 0 0;
  min-width: 20rem;
  border-radius: 50%;
  min-height: 20rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
  display: flex;
  /* justify-content: space-evenly; */
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
    min-width: 15rem;
    border-radius: 50%;
    min-height: 17rem;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
