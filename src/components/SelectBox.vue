<!-- 
https://vuejs.org/v2/guide/forms.html
https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
-->

<template>
  <div id="select-box">
    <div class="select">    <select v-model="selected">
      <option v-for="(option, index) in options" v-bind:value="option.value" v-bind:key="index">
        {{ option.text }}
      </option>
    </select>
    </div>
    <div class="button">
      <button>{{selected}}</button>
    </div>
  </div>
</template>

<script>

export default {
  name: 'select-box',
  data: function(){
    return {
      selected: 'A',
      options: [
        { text: 'search' , value: 'A' },
        { text: 'tagging', value: 'B' },
        { text: 'delete' , value: 'C' },
      ]
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

#select-box {
  width: 240px;
  /* background-color: dark-green;
  */
  background-color: lightblue;
}

.select {
  float: left;
}

.button {
  float: left;
}

</style>
