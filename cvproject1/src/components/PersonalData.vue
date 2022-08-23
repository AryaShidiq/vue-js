<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
    <div class="container border border-success border-4 rounded-3">
      <h3 class="text-center p-3">Personal Information</h3>
      <hr class="border border-warning border-1">
      <div class="row pt-1">
        <div class="col-md pb-2">
          <details>
            <summary>About Me</summary>
            I was born on 30th January 2005 in Jakarta.
            I'am a beginner web developer with basic web skills, advanced, to use laravel Framework. Always want to learn and improve.
          </details>
          <hr>
          <details>
            <summary>Contact</summary>
            Phone : +62 81274375824
            Email : aryashidiq30@gmail.com
          </details>
          <hr>
        </div>
        <div class="col-md pb-2">
          <details>
            <summary>Experience</summary>
            <ul>
              <li>Web Layouting With CSS Native</li>
              <li>Web Layouting with Bootstrap</li>
              <li>Teacher Agenda (Laravel)</li>
            </ul>
          </details>
          <hr>
          <details>
            <summary>Eduaction</summary>
            <ul>
              <li>SMK Taruna Bhakti Vocational School
                <br>
                In this School i learn how to designing web
              </li>
            </ul>
          </details>
          <hr>
        </div>
        <div class="col-md pb-2">
          <details>
            <summary>Language</summary>
            <ul>
              <li>Bahasa Indonesia
                <div class="progress-element progress-element--indonesia">
                  <div class="progress-container">
                    <progress max="100" value="100">100%</progress>
                  </div>
                </div>
              </li>
              <li>English
                <div class="progress-element progress-element--english">
                  <div class="progress-container">
                    <progress max="100" value="70">70%</progress>
                  </div>
                </div>
              </li>
            </ul>
          </details>
          <hr>
        </div>
      </div>
    </div>
    
  <!-- Template bawaan -->
  
  <!-- <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Documentation</template>

    Vue’s
    <a target="_blank" href="https://vuejs.org/">official documentation</a>
    provides you with all information you need to get started.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Tooling</template>

    This project is served and bundled with
    <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite</a>. The recommended IDE
    setup is <a href="https://code.visualstudio.com/" target="_blank">VSCode</a> +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>. If you need to test
    your components and web pages, check out
    <a href="https://www.cypress.io/" target="_blank">Cypress</a> and
    <a href="https://on.cypress.io/component" target="_blank"
      >Cypress Component Testing</a
    >.

    <br />

    More instructions are available in <code>README.md</code>.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ecosystem</template>

    Get official tools and libraries for your project:
    <a target="_blank" href="https://pinia.vuejs.org/">Pinia</a>,
    <a target="_blank" href="https://router.vuejs.org/">Vue Router</a>,
    <a target="_blank" href="https://test-utils.vuejs.org/">Vue Test Utils</a>, and
    <a target="_blank" href="https://github.com/vuejs/devtools">Vue Dev Tools</a>. If you need more
    resources, we suggest paying
    <a target="_blank" href="https://github.com/vuejs/awesome-vue">Awesome Vue</a>
    a visit.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Got stuck? Ask your question on
    <a target="_blank" href="https://chat.vuejs.org">Vue Land</a>, our official Discord server, or
    <a target="_blank" href="https://stackoverflow.com/questions/tagged/vue.js">StackOverflow</a>.
    You should also subscribe to
    <a target="_blank" href="https://news.vuejs.org">our mailing list</a> and follow the official
    <a target="_blank" href="https://twitter.com/vuejs">@vuejs</a>
    twitter account for latest news in the Vue world.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its sustainability. You can help
    us by
    <a target="_blank" href="https://vuejs.org/sponsor/">becoming a sponsor</a>.
  </WelcomeItem> -->

  <!-- Template bawaan -->


</template>

<style scoped>
h5{
  margin-top: 1rem;
}
li{
  list-style: square;
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
.progress-element--indonesia .progress-container::before {
  animation: progress-indonesia 1s ease-in forwards;
}
.progress-element--english .progress-container::before {
  animation: progress-english 1s ease-in forwards;
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

.progress-element--indonesia .progress-label::after {
  animation: progress-text-indonesia 1s ease-in forwards;
}

.progress-element--english .progress-label::after {
  animation: progress-text-english 1s ease-in forwards;
}

@keyframes progress-indonesia {
  to {
    width: 100%;
  }
}

@keyframes progress-english {
  to {
    width: 70%;
  }
}

@keyframes progress-text-indonesia {
  to {
    --num: 100;
  }
}

@keyframes progress-text-english {
  to {
    --num: 70;
  }
}
</style>
