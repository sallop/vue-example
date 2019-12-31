<!-- 
https://vuejs.org/v2/guide/forms.html
https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
https://vuejs.org/v2/api/#name
-->

<template>
  <div id="fixed-pane">
    <SelectBox></SelectBox>
    <InputForm></InputForm>
    <!--
    <ComponentA msg="fixed component A"></ComponentA>
    -->
  </div>
</template>

<script>
// import ComponentA from './components/ComponentA.vue'
// import ComponentA from './ComponentA.vue'
import SelectBox from './SelectBox.vue'
import InputForm from './InputForm.vue'

export default {
  name: 'fixed-pane',
  // data: function(){
  //   return {
  //     childMsg: "without pain, without sacrifice, we never nothing ..."
  //   }
  // },
  components: {
    // ComponentA,
    SelectBox,
    InputForm
    // child: {
    //   template: `<div>Hello Child Component</div>`,
    // }
  }
}

</script>

<style>
#fixed-pane {
  position: fixed;
  top: 0;
  /*
  width: 200px;
  bottom: 0;
  */
  background-color: white;
  border-style: solid;
  border-width: 2.5px;
  border-color: darkblue;
}
</style>
