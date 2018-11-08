<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <button @click="imp">加载一个组件</button>
    <div id="yhn"></div>
  </div>
</template>

<script>
import Vue from 'vue'
export default {
  name: 'HelloWorld',
  components:{
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },

  methods:{
    async imp(){
      let module=await import('@/components/yhn');
      let yhn=Vue.extend(module.default);
     new yhn({
       propsData:{
         bbb:"殷浩楠",
       },
       data:{
         msg:12345
       }
     }).$mount('#yhn');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
