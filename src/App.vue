<template>
  <div id="app">
    <h1>{{tittle1}}</h1>
    <h1 v-text="tittle2"></h1>
    <h1 v-html="tittle3"></h1>
    <ul>
      <li v-for="item in items" v-bind:class="{liclass,finished:item.isFinished}">{{item.label}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      tittle1: 'Hello Vue!<span>?</span>',
      tittle2: 'Hello Jyj!<span>?</span>',
      tittle3: 'Hello Gsy!<span>?</span>',
      items:[
        {
          label:'coding',
          isFinished:false
        },
        {
          label:'walk',
          isFinished:true
        }
      ],
      liclass:'liclass'
    }
  }
}
</script>

<style>
.finished{
  text-decoration:underline;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
