<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <MyHeader/>
    <OresContactForm/>
    <UserForm/>
    <TodoApp/> 
    <PhotoApp/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import OresContactForm from './components/OresContactForm.vue'
import UserForm from './components/UserForm.vue'
import TodoApp from './components/TodoApp.vue'
import PhotoApp from './components/PhotoApp.vue'






export default {
  name: 'app',
  components: {
     MyHeader,
    OresContactForm,
    UserForm,
    TodoApp,
    PhotoApp
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
