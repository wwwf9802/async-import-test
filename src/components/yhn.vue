<template>
  <div class="hello">
    yhnyhnyhnyhn
    <p>{{msg}}</p>
    <p>{{bbb}}</p>
  </div>
</template>

<script>
export default {
  name: 'yhn',
  props:{
    bbb:'',
  },
  data () {
    return {
      msg: '这里是yhnyhnyn'
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
