<template>
    <div id="son">
       <h1> I'm the child </h1>
       <h3 id="h3"> My name is: {{ nameAsProp }}</h3>
    </div>
</template>

<script>
export default {

    props: ['nameAsProp'],

    data() {
        return {
            name: 'Ariel'
        }
  },

  methods: {
      nameFromParent() {
          return this.nameAsProp;
      }
  }
}
</script>


<style>
 #son {
     width: 300px;
     height: 300px;
     background-color: lightcoral;
     font-size: 12px;
     display: flex;
     flex-direction: column;
     justify-content: center;
     align-items: center;
     border: 2px solid rgb(208, 32, 61)
    }

    #h3 {
        font-size: 15px; 
    }

    @import url('https://fonts.googleapis.com/css?family=Itim');
</style>


