<!-- 
https://vuejs.org/v2/guide/list.html 
https://vuejs.org/v2/guide/components.html#data-Must-Be-a-Function
https://vuejs.org/v2/guide/computed.html#Computed-Caching-vs-Methods
-->

<template>
  <div id="event-element">
    id:{{event.id}}
    object:{{event.object}}
    <button v-on:click='toggle()'>{{opend ? 'Close' : 'Open'}}</button>
    <div v-show="opend">{{event.description}}
    </div>
<!--
    <button v-on:click='opend=!opend'>{{opend}}</button>
    id:{{event.id}} {{event.object}} {{event.description}}
    <input type="checkbox" id="checkbox" v-model="checked[index]"/>
    id:{{event.id}} {{event.object}} {{event.description}}
    <button>Open:{{opend}}</button>
<ul>
  <li v-for="(event, index) in events" v-bind:key="index">
    <input type="checkbox" id="checkbox" v-model="checked[index]"/>
    id:{{event.id}} {{event.object}} {{event.description}}
    <button>Open</button>
    {{ checked }}:{{index}}
  </li>
</ul>
-->
</div>
</template>

<script>

export default {
  name: 'event-element',
  // props: ['event'],
  props: {
    event: Object
  },
  data: function(){
    return {
      opend: false
    }
  },
  methods: {
    toggle: function(){
      this.opend = !this.opend
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
