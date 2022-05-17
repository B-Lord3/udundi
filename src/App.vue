<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from '@/components/HelloWorld.vue'
import SocialIcons from '@/components/SocialIcons.vue'
</script>

<template>
  <div class="wrapper">
    <div class="hero">
      <div class="hero-bg">
        <HelloWorld msg="Explore" />
        <SocialIcons />
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
  width: 350px;
  height: 100%;
  background-color: #611818;
  position: absolute;
  top: 0;
  left: 0;
}

@media (hover: hover) {
  a:hover {
    /*background-color: hsla(160, 100%, 37%, 0.2);*/
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    /*display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;*/
  }
}
</style>
