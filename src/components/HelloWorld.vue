<template>
  <div class="hello">
    <div class="main">
      <h1>EmployeeNumber</h1>
      <input v-model="number" class="mainInput" />
    </div>
    <button @click="submit">提交</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      number:''
    }
  },
  methods: {
    submit(){
      if (!this.number){
        alert('Please Enter Your ID Num')
        return
      }
      this.$router.push({
        name:'Second',
        query:{
          number:this.number
        }
      })
    }
  },
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
  align-items:center;
}
.mainInput {
  height: 40px;
  margin-left:5px;
  font-size:20px;
}
</style>
