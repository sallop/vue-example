<!-- 
https://vuejs.org/v2/guide/forms.html
https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
https://vuejs.org/v2/api/#name
-->

<template>
  <div id="fixed-pane">
    Hello! Don't pay attention to me yet.
  </div>
</template>

<script>

export default {
  name: 'fixed-pane',
  data: function(){
    return {
      value: 0
    }
  }
}

</script>

<style>
#fixed-pane {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 200px;
  background-color: white;
  border-style: solid;
  border-width: 2.5px;
  border-color: darkblue;
}
</style>
