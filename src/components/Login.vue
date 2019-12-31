<!-- 
https://vuejs.org/v2/guide/forms.html
https://forum.vuejs.org/t/how-to-set-vue-instance-data-property-to-data-attribute/39219
-->
<template>
  <div id="login">
    username:
    <input
       v-model="username"
       placeholder="username"
       type="input-form"
    />
    <br/>
    password:
    <input
       v-model="password"
       placeholder="password"
       type="input-form"
    />
    <br/>
    <button v-on:click='login()'>login</button>
    <div>{{postdata}}</div>
  </div>
</template>

<script>

export default {
  name: 'login',
  // props: ['text'],
  data: function(){
    return {
      username: "",
      password: "",
      postdata: {
        username: "",
        password: "",
      },
    }
  },
  methods: {
    login: function(){
      this.postdata = {
        username: this.username,
        password: this.password,
      }
      return this.postdata
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
