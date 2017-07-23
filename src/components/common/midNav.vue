<template>
<div class="grid-content ">
        <el-row class="headerTool-col">
            <el-col :span="12" >
                    <el-input
                        class="mid-input"
                        placeholder="请选择搜索信息"
                        size="small"
                        icon="search"
                        v-model="search"
                        :on-icon-click="handleIconClick">
                    </el-input>
              </el-col> 
              <el-col :span="12">
                  <el-col :span="4"><img class="imgIcon" src="../../assets/photo/zoom+@2x.png"/></el-col> 
                  <el-col :span="4"><img class="imgIcon" src="../../assets/photo/zoom-@2x.png"/></el-col>
                  <el-col :span="4">
                      <!-- <img class="imgIcon" src="../../assets/photo/Group 2@2x.png"/> -->
                    <el-dropdown class="headerTool-dropdown" menu-align="start">
                        <span class="el-dropdown-link">
                          <img class="imgIcon" src="../../assets/photo/Group 2@2x.png"/>
                        </span>
                        <el-dropdown-menu slot="dropdown" class="headerTool-menu">
                            <el-dropdown-item class="headerTool-item">测量距离</el-dropdown-item>
                            <el-dropdown-item class="headerTool-item">面积测量</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                  </el-col>
                  <el-col :span="4">
                    <el-dropdown class="headerTool-dropdown" menu-align="start">
                        <span class="el-dropdown-link">
                          <img class="imgIcon" src="../../assets/photo/Group@2x.png"/>
                        </span>
                        <el-dropdown-menu slot="dropdown" class="headerTool-menu">
                            <el-dropdown-item class="headerTool-item">测量距离</el-dropdown-item>
                            <el-dropdown-item class="headerTool-item">面积测量</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>                  
                  </el-col>
                  <el-col :span="4"><img class="imgIcon" src="../../assets/photo/edit@2x.png"/></el-col> 
                  <el-col :span="4"><img class="imgIcon" src="../../assets/photo/export@2x.png"/></el-col> 
              </el-col> 
            </el-row>
    </div>
</template>

<script>
export default {
  name: 'midNav',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      search:"",
    }
  },
  methods:{
    handleIconClick(){
        alert("这是搜索框")
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .headerTool-col{
        height: 48px;
    }
    .imgIcon{
        display: inline-block;
        width: 24px;
        height: 24px;
        padding: 12px 10px 12px 10px;

    }
    .mid-input{
        margin-top:8px;
        height: 32px;
    }
    .headerTool-dropdown{
        display: inline-block;
        width: 24px;
        height: 24px;  
        color: #ffffff; 
    }
    .headerTool-menu{
        background: #505958;
        border: 0px;
        padding: 0;
        margin-top: 30px;
        color: #ffffff;
    }
    .headerTool-item:hover{
        background: #5EBF1D;
    }
</style>