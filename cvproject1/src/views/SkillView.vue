<script setup>
import Footer from '../components/Footer.vue';
import IconHtml from '../components/icons/IconHtml.vue';
import IconFigma from '../components/icons/IconFigma.vue';
import IconLaravel from '../components/icons/IconLaravel.vue';
import IconCss from '../components/icons/IconCss.vue';
import IconJavascript from '../components/icons/IconJavascript.vue';
import IconBootstrap from '../components/icons/IconBootstrap.vue';

</script>
<template>
  <div class="container border border-success border-4 rounded-3 mb-5 pt-5">
    
    <!-- SKILL PERCENTAGE BAR -->
    <div class="row">
      <h1 class="text-center pb-2"> What Can I Do...?</h1>
      <div class="col-md d-flex flex-column justify-content-center align-items-center">
        <!-- PROGRESS BARR -->
        
        <!-- HTML -->
        <div class="progress-element progress-element--html">
          <p class="progress-label"><IconHtml/></p>
          <div class="progress-container">
            <progress max="100" value="95">95%</progress>
          </div>
        </div>
        <!-- HTML CLOSED -->

        <!-- CSS -->
        <div class="progress-element progress-element--css">
          <p class="progress-label"><IconCss/></p>
          <div class="progress-container">
            <progress max="100" value="80">80%</progress>
          </div>
        </div>
        <!-- CSS CLOSED -->

        <!-- PROGRESS BARR CLOSED-->
      </div>
      <div class="col-md d-flex flex-column justify-content-center align-items-center" d-flex flex-column justify-content-center align-items-center>
        <!-- JAVA SCRIPT -->
        <div class="progress-element progress-element--javascript">
          <p class="progress-label"><IconJavascript/></p>
          <div class="progress-container">
            <progress max="100" value="65">65%</progress>
          </div>
        </div>
        <!-- JAVA SCRIPT CLOSED -->

        <!-- LARAVEL -->
        <div class="progress-element progress-element--laravel">
          <p class="progress-label"><IconLaravel/></p>
          <div class="progress-container">
            <progress max="100" value="70">70%</progress>
          </div>
        </div>
        <!-- LARAVEL CLOSED-->
      </div>
      <div class="col-md d-flex flex-column justify-content-center align-items-center">

        <!-- FIGMA -->
        <div class="progress-element progress-element--figma">
          <p class="progress-label"><IconFigma/></p>
          <div class="progress-container">
            <progress max="100" value="50">50%</progress>
          </div>
        </div>
        <!-- FIGMA CLOSED-->

        <!-- BOOTSTRAP -->
        <div class="progress-element progress-element--bootstrap">
          <p class="progress-label"><IconBootstrap/></p>
          <div class="progress-container">
            <progress max="100" value="80">80%</progress>
          </div>
        </div>
        <!-- BOOTSTRAP CLOSED-->

      </div>
    </div>
    <!-- SKILL PERCENTAGE BAR CLOSED -->
    <hr>
    <!-- PORTOFOLIO -->
    <h1 class="text-center p-3">Portofolio Session</h1>
    <div class="row">
      <div class="col-md p-3">
        <div class="card bg-dark" style="width: 18rem;">
          <img src="@/assets/agenda.png" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Agenda Guru (Laravel)</h5>
            <hr>
            <p class="card-text">Build up teacher agenda using laravel 9 and creative team admin template</p>
          </div>
        </div>
      </div>
      <div class="col-md p-3">
        <div class="card bg-dark" style="width: 18rem;">
          <img src="@/assets/cssnative.png" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Web Layout CSS Native</h5>
            <hr>
            <p class="card-text pb-4">Build up website  with CSS Native</p>
          </div>
        </div>
      </div>
      <div class="col-md p-3">
        <div class="card bg-dark" style="width: 18rem;">
          <img src="@/assets/bootstrap.png" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Web Layout Bootstrap</h5>
            <hr>
            <p class="card-text">Landing page of automotive website
            bootstrap really helpful here</p>
          </div>
        </div>
      </div>
    </div>
    <!-- PORTOFOLIO CLOSED-->
    <hr class="primary">
  </div>
  <footer>
    <Footer/>
  </footer>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Silkscreen&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Alumni+Sans+Pinstripe&display=swap');
h1{
  color: #CDF0EA;
  /* font-family: 'Silkscreen', cursive; */
  font-family: 'Alumni Sans Pinstripe', sans-serif;
}
progress {
  opacity: 0;
}

.progress-element {
  width: 200px;
  margin: 0 0 10px;
}

.progress-container {
  position: relative;
  background: #eee;
  height: 20px;
  border-radius: 6px;
  overflow: hidden;
}

.progress-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 0;
  background: turquoise;
}

.progress-element--html .progress-container::before {
  animation: progress-html 1s ease-in forwards;
}

.progress-element--css .progress-container::before {
  animation: progress-css 1s ease-in forwards;
}

.progress-element--javascript .progress-container::before {
  animation: progress-javascript 1s ease-in forwards;
}
.progress-element--laravel .progress-container::before {
  animation: progress-laravel 1s ease-in forwards;
}
.progress-element--figma .progress-container::before {
  animation: progress-figma 1s ease-in forwards;
}
.progress-element--bootstrap .progress-container::before {
  animation: progress-bootstrap 1s ease-in forwards;
}

.progress-label {
  position: relative;
}

@property --num {
  syntax: "<integer>";
  initial-value: 0;
  inherits: false;
}

.progress-label::after {
  counter-reset: num var(--num);
  content: counter(num) "%";
  position: absolute;
  top: 0;
  right: 0;
}

.progress-element--html .progress-label::after {
  animation: progress-text-html 1s ease-in forwards;
}

.progress-element--css .progress-label::after {
  animation: progress-text-css 1s ease-in forwards;
}

.progress-element--javascript .progress-label::after {
  animation: progress-text-javascript 1s ease-in forwards;
}
.progress-element--laravel .progress-label::after {
  animation: progress-text-laravel 1s ease-in forwards;
}
.progress-element--figma .progress-label::after {
  animation: progress-text-figma 1s ease-in forwards;
}
.progress-element--bootstrap .progress-label::after {
  animation: progress-text-bootstrap 1s ease-in forwards;
}

@keyframes progress-html {
  to {
    width: 95%;
  }
}

@keyframes progress-css {
  to {
    width: 60%;
  }
}

@keyframes progress-javascript {
  to {
    width: 30%;
  }
}
@keyframes progress-laravel {
  to {
    width: 60%;
  }
}
@keyframes progress-figma {
  to {
    width: 50%;
  }
}
@keyframes progress-bootstrap {
  to {
    width: 95%;
  }
}

@keyframes progress-text-html {
  to {
    --num: 95;
  }
}

@keyframes progress-text-css {
  to {
    --num: 60;
  }
}

@keyframes progress-text-javascript {
  to {
    --num: 30;
  }
}
@keyframes progress-text-laravel {
  to {
    --num: 60;
  }
}
@keyframes progress-text-figma {
  to {
    --num: 50;
  }
}
@keyframes progress-text-bootstrap {
  to {
    --num: 95;
  }
}
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
