<template>
    <div>
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="1">关于</el-menu-item>
        <el-submenu index="2">
        <template slot="title">我的工作台</template>
        <el-menu-item index="2-1">选项1</el-menu-item>
        <el-menu-item index="2-2">选项2</el-menu-item>
        <el-menu-item index="2-3">选项3</el-menu-item>
        </el-submenu>
        <el-menu-item index="3">VMES 2.0</el-menu-item>
        <el-menu-item index="4">平台服务</el-menu-item>
        
    </el-menu>
    <!-- 这里加个判断index等于几显示几 -->
        <div class="massg">
            <img style="width: 100%; height: 100%;" src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png">
        </div>
        
        <div class="juz">
            <span>124</span>
            <span>123789</span>
            <img style="width: 150px; height: 150px;" src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png" >
        </div>
        
        <div class="asd">
        <div class="choice">
        <el-row>
            <el-col :span="4"  v-for="item in options" :key="item.value" :offset="item.value > 0 ? 2 : 0">
                <el-card shadow="hover" :body-style="{ padding: '20px' }">
                    <img src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png" class="image">
                    
                    <div style="padding: 0px;">
                    <span>{{item.label}}</span>
                    </div>
                </el-card>
            </el-col>
        </el-row>
        </div>
        </div>
        <div class="asd">
        <div class="choice">
        <el-row>
            <el-col :span="4"  v-for="item in options" :key="item.value" :offset="item.value > 0 ? 2 : 0">
                <el-card shadow="hover" :body-style="{ padding: '20px' }">
                    <img src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png" class="image">
                    
                    <div style="padding: 0px;">
                    <span>{{item.label}}</span>
                    </div>
                </el-card>
            </el-col>
        </el-row>
        </div>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'Dashboard',
    data() {
      return {
          options: [{
          value: '1',
          label: '点1',
          img:'',
        }, {
          value: '2',
          label: '点1',
          img:'',
        },
        {
          value: '3',
          label: '点3',
          img:'',
        },
        {
          value: '4',
          label: '点4',
          img:'',
        },
        ],
        activeIndex: '1',
        activeIndex2: '1',
        index: '',
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  
}
</script>

<style scoped>
.asd{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 20px;
}
    .juz{
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .choice{
        width: 50%;
        
    }
    .massg{
        width: 100%;
        height: 400px;
    }


  .image {
    width: 100%;
    display: block;
  }

 
</style>