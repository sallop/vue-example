<template>
  <div id="app">
    <!--
      img alt="Vue logo" src="./assets/logo.png"
      <HelloWorld msg="Welcome to Your Vue.js App"/>
      <ComponentA msg="ComponentA"/>
      <SelectBox/>
    <CheckBox text="new text"/>
    -->
    <Login/>
    <List></List>
    <FixedPane></FixedPane>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import ComponentA from './components/ComponentA.vue'
// import SelectBox from './components/SelectBox.vue'
// import CheckBox from './components/CheckBox.vue'
import List from './components/List.vue'
import FixedPane from './components/FixedPane.vue'
import Login from './components/Login.vue'

export default {
  name: 'app',
  components: {
    //ComponentA,
    //SelectBox,
    //CheckBox,
    List,
    FixedPane,
    Login
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
