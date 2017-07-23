<template>
      <div id="headerTool">
          <el-row class="headerTool-col">
            <el-col :span="11" class="headerTool-col">
                <img class="imglogo" src="../../assets/photo/title@1x.png"/>
            </el-col>
            <el-col :span="10" class="headerTool-col">
              <midNav></midNav>
            </el-col>
            <el-col :span="3" class="headerTool-col">  
                <div id="rn">
                <ul>
                    <li><img class="r-img"src="../../assets/photo/home@2x.png" @click="routerGo('/')"/></li>    
                    <li><img class="r-img"src="../../assets/photo/user@2x.png" @click="routerGo('/userinfo')"/></li>    
                    <li><img class="r-img"src="../../assets/photo/logout@2x.png"   @click="logout()"/></li> 
                </ul> 
                </div>
            </el-col>
          </el-row>
      </div>    
</template>
<script>
import midNav from './midNav.vue'

export default {
    name: 'headerTool',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      signupActive:'',
    }
  },
  components:{
    midNav,
  },
  methods:{
    routerGo(url){
        this.$router.push(url);
      },
    logout(){
      var _this = this;
       this.$confirm('确认退出吗?', '提示', {
					//type: 'warning'
				})
          .then(function(){
              sessionStorage.removeItem('user');
              _this.$router.push('/signin');
          });
    }
  },
}
</script>
<style scoped>
#headerTool{
  background: #505958;
}
#rn{
  background-color:  rgba(41,51,50,0.30);  
  text-align: center;
  height:48px
}
.headerTool-col{
      height:48px
}
li{
    list-style-type:none;
    display: inline-block;
}
.r-img{
    display: inline-block;
    width: 24px;
    height: 24px;
    padding: 10px 10px ;
}
.imglogo{
  display: inline-block;
  height: 28px;
  padding:10px 24px;
}
</style>
