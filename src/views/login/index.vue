<template>
  <div>
    123456789
    <el-button type="primary" @click="btn">主要按钮</el-button>
  </div>
</template>

<script>

export default {
  name: 'Login',
  data() {
    
    
    
    
    // return {
    //   show:true,
      
    //   //忘记密码模块
      
      
    //   loading: false,
    //   passwordType: 'password',
    //   redirect: undefined
    // }
  },
  // watch: {
  //   $route: {
  //     handler: function(route) {
  //       this.redirect = route.query && route.query.redirect
  //     },
  //     immediate: true
  //   }
  // },
  methods: {
    // tip(){
    //   this.show = !this.show
    // },
    
    
    
    //登录
    btn() {
                this.$message({
              showClose: true,
              message: '登录成功',
              type: 'success'
            });
            this.$router.push({ path:  '/src/views/dashboard/index.vue' })
              
    },
  }
}
</script>


<style scoped>

</style>