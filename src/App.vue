<template>
  <div id="app">
    <button @click="toonBoodschap">Open modal</button>
    <transition name="modal">
      <cvo-modal v-if="modalOpen" :titel="titel" :boodschap="boodschap" @close="modalOpen = false"/>
    </transition>
  </div>
</template>

<script>
import CvoModal from './components/CvoModal.vue'

export default {
  name: 'app',
  data() {
    return {
      modalOpen: false,
      titel: "",
      boodschap: "",
    }
  },
  components: {
    CvoModal
  },
  methods: {
    toonBoodschap() {
      this.modalOpen = true;
      this.titel = "Welkom";
      this.boodschap = "Deze modal is een herbruikbare component";
    }
  },
}
</script>

<style>
.modal-enter, .modal-leave-to {
  opacity: 0;
}

.modal-enter-active, .modal-leave-active {
  transition: opacity .5s;
}
</style>
