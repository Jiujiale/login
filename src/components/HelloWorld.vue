<template>
  <div class="hello">
    <div class="main">
      EmployeeNumber
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

.main {
  font-family:Microsoft YaHei;
  display:flex;
  flex-direction:row;
  width:100%;
  font-size:16px;
  font-weight:bold;
  align-items:center;
}
.mainInput {
  height: 30px;
  margin-left:5px;
  width:150px;
  font-size:16px;
}
</style>
