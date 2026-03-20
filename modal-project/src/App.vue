<template>
  <h1>{{ title }}</h1>
  <p>Welcome</p>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Lien 1</a>
        <a href="#">Lien 2</a>
      </template>
      <h1>Titre</h1>
      <p>Contenu</p>
    </Modal>
  </div>
  <div v-if="showModal2">
    <Modal @close="toggleModal2">
      <template v-slot:links>
        <a href="#">Lien 3</a>
        <a href="#">Lien 4</a>
      </template>
      <h1>Titre</h1>
      <p>Contenu</p>
    </Modal>
  </div>
  <button @click="toggleModal()">Open Modal</button>
  <button @click="toggleModal2()">Open Modal 2</button>
</template>

<script>
  import Modal from './components/Modal.vue'

  export default {
    name: 'App',
    components: { Modal },
    data() {
      return {
        title: 'My First Vue App!',
        header: 'This is the header',
        text: 'This is the text',
        showModal: false,
        showModal2: false
      }
    },
    methods: {
      toggleModal() {
        this.showModal = !this.showModal
      },
      toggleModal2() {
        this.showModal2 = !this.showModal2
      }
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
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
