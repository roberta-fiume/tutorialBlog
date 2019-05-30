<template>
  <div id="app">
       <h1> I'm the parent </h1>
       <h3 id="name"> My name is: {{ name}}</h3>
       <button id="button1" v-on:click="changeName"> Change name in my son</button>
    <child-component :nameAsProp="name"></child-component>
  </div>
</template>

<script>
 import ChildComponent from  "./ChildComponent.vue";
  export default {
  data() {
    return {
      name: 'Jack'
    }
  },

  methods: {
    changeName() {
     return this.nameAsProp;
      console.log("name",this.nameAsProp)
    }
  },

  components: {
    "child-component": ChildComponent
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css?family=Raleway:100,300,500,700');

html, body {
  font-family: 'Raleway', sans-serif;
}

body {
  font-family: 'Raleway', sans-serif;
}

#app {
  width: 900px;
  height: 700px;
  background-color: lightseagreen;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'Itim', cursive;
  border: 2px solid rgb(20, 98, 80);
}

#name {
  font-size: 18px; 
}


#button1 {
  width: 200px;
  height: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'Itim', cursive;
  background-color: #6AC0BD;
  border: 2px solid #0F4442;
  margin-bottom: 30px;
} 
</style>
