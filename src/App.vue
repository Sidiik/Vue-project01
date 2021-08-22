<template>
  <h1>{{ title }}</h1>
  <teleport to=".modals" v-if="showModal">
    <Modal theme="" @close="openModal">
      <h1>
        Sadiq's give away
      </h1>
      <p>Get your way of happiness</p>
      <template v-slot:links>
        <a href="#">Get our the info</a>
      </template>
    </Modal>
  </teleport>
  <teleport to=".modals" v-if="showModalTwo">
    <Modal theme="" @close="openModalTwo">
      <h1>
        Sadiq's give away Two
      </h1>
      <p>Get your way of happiness</p>
      <template v-slot:links>
        <a href="#">Get our the info</a>
      </template>
    </Modal>
  </teleport>
  <button @click="openModal">Open modal</button>
  <button @click="openModalTwo">Open modal Two</button>
</template>

<script>
import Modal from "./components/Modal";

export default {
  name: "App",
  components: { Modal },
  data() {
    return {
      header: "this is the new success range",
      text: "texted ",
      title: "Welcome to my first vue app",
      showModal: false,
      showModalTwo: false,
    };
  },
  methods: {
    openModal() {
      this.showModal = !this.showModal;
    },
    openModalTwo() {
      this.showModalTwo = !this.showModalTwo;
    },
  },
};
</script>

<style>
#app,
.modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
