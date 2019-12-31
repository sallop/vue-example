<!-- 
https://vuejs.org/v2/guide/forms.html
https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
-->
<template>
  <div id="input-form">
    <input
       v-model="text"
       placeholder="search key"
       type="input-form"
    >
    <!--
       true-value="yes"
       false-value="no"
    -->
    <div>{{text}}</div>
  </div>
</template>

<script>

export default {
  name: 'input-form',
  // props: ['text'],
  data: function(){
    return {
      text: "",
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
