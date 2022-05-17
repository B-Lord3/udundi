<script setup>
import SocialItem from './SocialItem.vue'
import FacebookIcon from './icons/IconFacebook.vue'
import InstagramIcon from './icons/IconInstagram.vue'
</script>

<template>
  <div class="social-icons">
    <a href="#facebook">
      <SocialItem>
        <template #icon>
          <FacebookIcon />
        </template>
      </SocialItem>
    </a>

    <a href="#instagram">
      <SocialItem>
        <template #icon>
          <InstagramIcon />
        </template>
      </SocialItem>
    </a>
  </div>
</template>

<style>
  .social-icons {
    display: flex;
    flex-direction: column;
    gap: 20px;
    position: absolute;
    right: 40px;
    bottom: 40px;
  }

  .social-icons i {
    width:  65px;
    height: 65px;
  }
</style>
