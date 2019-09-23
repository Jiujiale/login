<template>
  <div class="hello">
    <div class="main">
      {{number}} Check in successful,code is {{code}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      number:'',
      code:''
    }
  },
  created() {
  },
  mounted() {
    this.number = this.$route.query.number    
    document.title = 'Check in Success'
    this.code = '98' + new Date().getDate()
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
.main {
  font-size:40px;
  font-weight:bold;
}
</style>
