<template>
  <div id="app">
    <button @click="toonBoodschap">Open modal</button>
    <cvo-modal :open="isOpen" :titel="titel" :boodschap="boodschap" @close="isOpen = false"/>
  </div>
</template>

<script>
import CvoModal from './components/CvoModal.vue'

export default {
  name: 'app',
  data() {
    return {
      isOpen: false,
      titel: "",
      boodschap: ""
    }
  },
  components: {
    CvoModal
  },
  methods: {
    toonBoodschap() {
      this.isOpen = true;
      this.titel = "Welkom";
      this.boodschap = "Deze modal is een herbruikbare component";
    }
  },
}
</script>

<style>

</style>
