<script>
  import TitleExplore from '@/components/headings/TitleExplore.vue'
  import SocialItem from './SocialItem.vue'
  import PlusIcon from './icons/IconPlus.vue'
  import ModalAlert from './modal/ModalAlert.vue'

  export default {
    props: {
      msg: {
        type: String, 
        required: true
      },
      visible: Boolean,
    },
    components: {
      TitleExplore,
      SocialItem,
      PlusIcon,
      ModalAlert,
    },
    data() {
      return {
        showMsg: false
      }
    },
    computed: {
      showModal() {
        this.showMsg = true;
        console.log(this.showMsg)
      }
    }
  }
</script>

<template>
  <div class="greetings">
    <div class="col col-lg-4 sidebar position-absolute"></div>
    <div class="container">
      <div class="row">
        <div v-if="!showMsg">
          <!-- <h1 class="page-title">{{ msg }}</h1> -->
          <TitleExplore />
          <div class="btn-container">
            <SocialItem>
              <template #icon>
                <button v-on:click="showModal" class="btn-plus">
                  <PlusIcon />
                </button>
              </template>
            </SocialItem>
            
            <span class="btn-section-title">More Details</span>
          </div>
        </div>
        <div v-else>
          <ModalAlert :msg="modalMsg" :visible="showMsg" />
        </div>
      </div>
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
  position: relative;
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
  justify-content: flex-start;
  gap: 20px;
  margin-left: 8%;
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

button.btn-plus {
  padding: 0;
  border-radius: 50%;
  box-shadow: 0px 0px 0px 0px rgba(255, 255, 255, 1);
  transition: all 0.5s;
}

button.btn-plus:hover {
  box-shadow: 0px 0px 0px 10px rgba(255, 255, 255, 0.2);
}

.modal {
  /*display: flex;*/
  width: 50px;
  height: 50px;
  left: 0;
  bottom: 0;
  position: absolute;
}

.card {
  width: 100%;
  max-width: 500px;
  padding: 40px 20px;
  background-color: var(--vt-c-white);
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.card h1 {
  color: #611818;
  font-size: 66px;
}
.card h1:after {
  width: 100%;
  height: 3px;
  background-color: #611818;
}


@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
