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
-->

<template>
  <div id="event-list">
  <ul>
    <li v-for="(event, index) in events" v-bind:key="index">
      <input type="checkbox" id="checkbox" v-model="checked"/>
      id:{{event.id}} {{event.object}} {{event.description}}
      <button> {{ event.id }} </button>
      {{ checked }}
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

export default {
  name: 'event-list',
  // props: ['events'],
  data: function(){
    return {
      events: [{
        id: "1",
        object: "object1",
        description: "description"
      },{
        id: "2",
        object: "object2",
        description: "description"
      },{
        id: "3",
        object: "object3",
        description: "description"
      }],
      checkedNames: []
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
