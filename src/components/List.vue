<!-- 
https://vuejs.org/v2/guide/list.html 
https://vuejs.org/v2/guide/components-slots.html
https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_templates_and_slots
      <label for="checkbox">{{ checked }}</label>
https://medium.com/vue-by-example/learn-quickly-working-with-a-list-of-checkboxes-348c16548a99
https://codepen.io/patrickodacre/pen/PjWKbo
https://www.freecodecamp.org/news/an-introduction-to-dynamic-list-rendering-in-vue-js-a70eea3e321/
https://vuejs.org/v2/guide/forms.html
  https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
  vue.js simple tuts: toggling
  https://medium.com/@codebyjeff/vue-js-simple-tuts-toggling-b80edddee1ac
-->


<template>
  <div id="event-list">
  <ul>
    <li v-for="(event, index) in events" v-bind:key="index">
      <Element v-bind:event="event"></Element>
<!--
      <element event=e></element>
      <input type="checkbox" id="checkbox" v-model="checked[index]"/>
  id:{{event.id}} {{event.object}} {{event.description}}
  <button>Open</button>
  {{ checked }}:{{index}}
-->
    </li>
  </ul>
</div>
</template>

<!--
<template slot="name" slot-scope="props">
  <span :class="{selected:props.item.selected}">
    {{props.item.name}}
  </span>
</template>

<template slot="selected" slot-scope="props">
  <input type="checkbox" v-model="props.item.selected">
</template>
-->



<script>
// import Element from './components/Element.vue'
import Element from './Element.vue'



export default {
  name: 'event-list',
  // props: ['events'],
  components: {
    Element
  },
  data: function(){
    return {
      events: [{
        id: "11",
        object: "object1",
        description: "description11"
      },{
        id: "12",
        object: "object2",
        description: "description12"
      },{
        id: "13",
        object: "object3",
        description: "description13"
      },{
        id: "14",
        object: "object3",
        description: "description14"
      },{
        id: "15",
        object: "object3",
        description: "description5"
      },{
        id: "16",
        object: "object3",
        description: "description16"
      },{
        id: "17",
        object: "object3",
        description: "description17"
      },{
        id: "18",
        object: "object3",
        description: "description18"
      },{
        id: "19",
        object: "object3",
        description: "description19"
      },{
        id: "20",
        object: "object3",
        description: "description20"
      },{
        id: "21",
        object: "object3",
        description: "description21"
      }
      ],
      // checkedNames: []
      // checked: ['elem0', 'elem1', 'elem2']
      // checked: true
      checked: []
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

ul {
  list-style-type: none;
}

</style>
