<script setup>
import TitleExplore from '@/components/icons/TitleExplore.vue'
import SocialItem from './SocialItem.vue'
import PlusIcon from './icons/IconPlus.vue'

defineProps({
  msg: {
    type: String, 
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <div class="sidebar"></div>
    <!-- <h1 class="page-title">{{ msg }}</h1> -->
    <TitleExplore />
    <div class="btn-container">
        <SocialItem>
          <template #icon>
            <button>
              <PlusIcon />
            </button>
          </template>
        </SocialItem>
      
      <span class="btn-section-title">More Details</span>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 10rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings {
  width: 100%;
  padding: 200px 100px;
  display: flex;
  align-items: flex-start;
  justify-content: flex-end;
  flex-direction: column;
}

.greetings h1,
.greetings h3 {
  text-align: center;
  color: #fff;
}

.page-title {
  line-height: 1;
}

.btn-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  margin-left: 30px;
}

.btn-section-title {
  color: var(--vt-c-white);
  font-size: 25px;
}

  button {
    cursor: pointer;
    align-content: normal;
    border: transparent;
    background: transparent;
  }

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
