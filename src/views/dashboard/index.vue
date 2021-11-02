<template>
    <div>
      <div style="position: fixed;width: 100%;height: 80px;top:0;background: white;display: flex;">
        <img src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png" style="width: 50px; height: 50px;margin: 10px 15px;" >
    <el-menu :default-active="activeIndex" class="el-menu-demo" style="border-bottom:none;" mode="horizontal" @select="handleSelect" >
        <el-menu-item index="1">关于</el-menu-item>
        <el-submenu index="2">
        <template slot="title">我的工作台</template>
        <el-menu-item index="2-1">选项1</el-menu-item>
        <el-menu-item index="2-2">选项2</el-menu-item>
        <el-menu-item index="2-3">选项3</el-menu-item>
        </el-submenu>
        <el-menu-item index="3">VMES 2.0</el-menu-item>
        <el-menu-item index="4">平台服务</el-menu-item>
        <div style="margin: 0 0 0 928px;display:inline;">
        <el-button style="color: #000;" type="text">返回首页</el-button>
        <el-button style="color: #000;" type="text">？？入口</el-button>
        <div style="margin: 0;display:inline;">
        <el-button style="margin:0;border-right: 1px solid black;padding: 3px 5px;" type="text">登录</el-button>
        
        <el-button style="margin:0;" type="text">退出</el-button>
        </div>
        </div>
    </el-menu>
    
    </div>
    <!-- 这里加个判断index等于几显示几 -->
        <div class="massg">
            <img style="width: 100%; height: 100%; margin-top:80px" src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png">
        </div>
        
        <div class="juz">
          <div style="margin-top:80px">
            <span style="font-size: 40px;font-weight: bold;">鲸科云</span>
            <span><p style="text-indent: 2em">仕泰隆鲸科云平台通过自主研发的设备数据采集器和VMES可视化生产管理系统,为金属加工行业的中小企业提供一站式数字化解决方案。通过“硬件+软件产品的标准化、模块化、轻量化设
						计及嵌入式算法的高速送代,打造一套PLC体外平行数字仿真系统”,大大降低企业数字化转型实施成本,可快速提高中小企业数字化普及率。</p></span>
						<div style="display: flex;">
              <span><p style="text-indent: 2em">平台在边缘节点通信能力、协议转换、边缘运维、数据预处理。模型管理、安全性能等数据处理及验算能力,已通过中国信通院专家测评并得到高度认可</p>
						<p style="text-indent: 2em">鲸科云平台产品广泛应用于机床、注塑、冲压、钣金激光、机器人、检测设备等,能满足车间所有设备上云,通过产品标准化、模块化、轻量化、批量
					化,具备可复制性,可快速批量为智能制造企业设备上云上平台平台通过大数据建模分析,不断拓展工业大数据的应用场景实现产能共享、金融创新、
					行业指数发布、供应链协同等一站式增值服务构建工业互联网赋能智能制造的全方位生态体系。</p>
						<p style="text-indent: 2em">使命为工业强国而战理念开放协同创新目标:中小企业数字化平台领跑者方针:全员营销全员客服。</p></span>
            <img style="width: 100px; height: 100px; margin: 40px 0px 0px 10px;" src="https://i.loli.net/2021/10/27/HDGMuaYylQT3bvk.png" ></div>
          </div>
            
        </div>
        <div style="margin:20px 280px;font-size: 40px;font-weight: 500;">功能模块菜单</div>
        <div class="asd">
        <div class="choice">
        <el-row>
            <el-col :span="4"  v-for="item in options" :key="item.value" :offset="item.value > 0 ? 2 : 0">
              <el-button type="text" @click="buts(item.value)">
                <el-card shadow="hover" :body-style="{ padding: '20px' }">
                    <img :src="item.img" class="image">
                    
                    <div style="padding: 0px;">
                    <span>{{item.label}}</span>
                    </div>
                </el-card>
              </el-button>
            </el-col>
        </el-row>
        </div>
        </div>
        <div class="asd">
        <div class="choice">
        <el-row>
            <el-col :span="4" v-for="item in options2" :key="item.value" :offset="item.value > 0 ? 2 : 0">
              <el-button type="text" @click="buts(item.value)">
                <el-card shadow="hover" :body-style="{ padding: '20px' }">
                    <img :src="item.img" class="image">
                    
                    <div style="padding: 0px;">
                    <span>{{item.label}}</span>
                    </div>
                </el-card>
              </el-button>
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
          img:require('../../image/111.png'),
        }, {
          value: '2',
          label: '点1',
          img:require('../../image/111.png'),
        },
        {
          value: '3',
          label: '点3',
          img:require('../../image/111.png'),
        },
        {
          value: '4',
          label: '点4',
          img:require('../../image/111.png'),
        },
        ],
        options2: [{
          value: '1',
          label: '点1',
          img:require('../../image/111.png'),
        }, {
          value: '2',
          label: '点1',
          img:require('../../image/111.png'),
        },
        {
          value: '3',
          label: '点3',
          img:require('../../image/111.png'),
        },
        {
          value: '4',
          label: '点4',
          img:require('../../image/111.png'),
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
      },
      buts(res){
        console.log(res)
        console.log(123)
      }
    }
  
}
</script>

<style scoped>
.el-button {
  margin: 20px 20px;
  
}

  

.asd{
    
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 20px;
}
    .juz{
      
        /* width: 100%; */
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 40px 280px;
    }
    .juz>div>span:nth-child(1){
      /* position: relative; */
      /* top: 30px; */
      /* left: 50%; */
    }
    /* .juz>div>span:nth-child(2){
      width: 60%;
    } */
    
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