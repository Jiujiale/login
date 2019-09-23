<template>
  <div class="hello">
    <div class="main">
      <h1>EmployeeNumber</h1>
      <input class="mainInput" />
    </div>
    <button>提交</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
.main {
  display:flex;
  flex-direction:row;
  width:100%;
  background:'red';
  align-items:center;
}
.mainInput {
  height: 40px;
  margin-left:5px;
}
</style>
