<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from '@/components/HelloWorld.vue'
import SocialIcons from '@/components/SocialIcons.vue'

// Import Bootstrap and BootstrapVue CSS files (order is important)
import 'bootstrap/dist/css/bootstrap.css'

</script>

<template>
  <div class="container-fluid">
    <div class="row">
      <div class="wrapper">
        <div class="hero">
          <div class="hero-bg">
            <HelloWorld msg="Explore" />
            <SocialIcons />
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- <RouterView /> -->
</template>

<style>
@import '@/assets/base.css';

#app {
  width: 100%;
  height: auto;
  display: flex;

  font-weight: normal;
}

.wrapper {
  width: 100%;
  height: auto;
  padding: 0;
}

.hero {
  width: 100%;
  height: 100vh;
  display: flex;
}

.hero-bg {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row;
  position: relative;
  background-image: url('@/assets/Coding-Challenge-Image.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  transition: all 0.5s;
}

.hero-bg .sidebar {
  /*width: 350px;*/
  height: 100%;
  background-color: #611818;
  top: 0;
  left: 0;
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }
}
</style>
