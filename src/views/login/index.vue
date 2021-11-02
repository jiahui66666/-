<template>
  <div>
    123456789
    <el-button :plain="true" :loading="loading" type="primary" @click.native.prevent="btn">主要按钮</el-button>
  </div>
</template>

<script>

export default {
  name: 'Login',
  data() {
    
    
    
    
    return {
    //   show:true,
      
    //   //忘记密码模块
      
      
      loading: false,
    //   passwordType: 'password',
    //   redirect: undefined
    }
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
          message: '恭喜你，这是一条成功消息',
          type: 'success'
        });
            this.$router.push({ path:  '/src/views/dashboard/index.vue' })
              loading: false
    },
  },
}
</script>


<style scoped>

</style>