<!-- 
https://vuejs.org/v2/guide/forms.html
https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
-->

<template>
  <div id="checkbox">
    <input
       type="checkbox"
       v-model="toggle"
       true-value="yes"
       false-value="no"
    >
    <div>{{text}}</div>
  </div>
</template>

<script>

export default {
  name: 'checkbox',
  props: ['text'],
  data: function(){
    return {
      value: 0
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
