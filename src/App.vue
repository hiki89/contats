<template>
  <div id="app">
    <NavBar />
    <!-- <ContactList :title="parentTitle" @parentMtd="parentMethod"/> -->
    <router-view></router-view>
    <!-- <img src="./assets/logo.png"> -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ContactList from './components/ContactList.vue';
import NavBar from './components/NavBar.vue';

export default {
  name: 'app',
  data() {
    return {
    parentTitle: 'Contact list parent'
    }
  },
  components: {
    HelloWorld,
    ContactList,
    NavBar
  },
  methods: {
    parentMethod(value) {
      console.log(value);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
