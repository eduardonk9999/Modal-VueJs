<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal 
      header="Sign up for the Giveaway!" 
      text="Grab you" 
      :text3="text3" 
      theme="sale" 
      @close="toggleModal"
    >
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Ninja Vue</h1>
      <p>Grab your ninja swag</p>
    </Modal>
  </div>
  <button @click="toggleModal">Open Modal</button>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      title: "My First Vue App :)",
      text3: "sou uma prop",
      showModal: false
    };
  },
  methods: {
    toggleModal(){
      this.showModal  = !this.showModal
    }
  }
};
</script>

<style>
  #app {
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  h1 {
    border-bottom: 1px solid #ddd;
    display: inline-block;
    padding-bottom: 10px;
  }
</style>
