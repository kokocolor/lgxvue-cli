<template>
  <div id="app">

    <img src="./images/detail.jpg">
    <div >我的详情</div>
    <br/>
      <p v-for="n in pageCount">
                    <a href="javascripit:void(0)" v-bind:class="activeNumber === n + 1 ? 'active' : ''" v-on:click="greet">{{ n + 1 }}</a>
                </p>
    <wo></wo>
  </div>
</template>

<script>
  import 'common/css/reset.css';
  import wo from 'components/Hello/Wo'

  export default {
    name: 'app', 
     data() {
        return {
           activeNumber: 2,
           pageCount: 10
        }
       },
      methods: {
              greet: function() {
                  // // 方法内 `this` 指向 vm
                  alert(this.activeNumber)
              },
              say: function(msg) {
                  alert(msg)
              }
          },
    components: {
      wo
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
  .active{
  color:green;
  }
</style>
