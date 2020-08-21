<template>
  <div id= 'app'>
    <input type="text" v-model="text" id="inp">
    <button @click="add">Add todo</button>
    <ul >
      <li v-for="(item,i) in array" :key="i">
      {{item}}
      <button @click="remove(i)">remove</button>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',


  data(){
  return {
    array :[],
    text:''
    }
  },

  methods: {
    add(){
      this.array.push(this.text)
    },
    remove(i){
      this.array.splice(i,1);
    }

  }
}
</script>

<style>
#inp {
  text-align: center;
  color: grey;
  margin-top: 60px;
}
</style>
