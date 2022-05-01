<template>
  <p>Hello There</p>
  <div v-if="showModal">
    <Modal theme="sale">

      <!-- Dynamic slot / It must have a name that we will use to call it in the main component are  -->
      <template v-slot:links>
        <a href="#">The Maxwel</a>
        <a href="#">The Ochieng</a>
    </template>
      <div>
        <h1>Hello Maxwel</h1>
        <p>Grab your deal from KFC now</p>
      </div>
    </Modal>
  </div>
  <span @click="handleShow">
    <button v-if="!showModal">Show Modal</button>
    <br /><br />
    <button v-show="showModal">Hide Modal</button>
  </span>
</template>

<script>
import Modal from "../src/components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      header: "Hello Maxwel",
      text: " Grab your deal from KFC now",
      showModal: false,
    };
  },
  methods: {
    handleShow() {
      this.showModal = !this.showModal;
    },
  },
  components: {
    Modal,
  },
};
</script>

<style>
#app {
  margin: 0;
  padding: 0;
}
</style>
