<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings p-3">
    <!-- NAVBAR -->
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container-fluid">
          <a class="navbar-brand me-5" href="#">CV</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse ms-5" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0 router d-flex justify-content-evenly">
              <li class="nav-item">
                <RouterLink to="/">Personal Info</RouterLink>
              </li>
              <li class="nav-item">
                <RouterLink to="/Skill">SKill</RouterLink>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    <div class="info p-3">
      <h1 class="text-center pt-2">Ciao!</h1>
      <hr>  
      <div class="hello">
        <h2 class="p-3">My Name Is Arya Shidiq</h2>
        <h2 class="p-3">And I'am A Backend Web Developer</h2>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Aboreto&display=swap');
h1{
  font-family: 'Aboreto', cursive;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}
h2{
  font-family: 'Alumni Sans Pinstripe', sans-serif;
}
.greetings h1,
.greetings h3 {
  text-align: center;
}
nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
.navbar-nav{
  gap: 2rem;
}
</style>
