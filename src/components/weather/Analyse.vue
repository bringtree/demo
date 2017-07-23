<template>
  <div id="analyse">
      <div class="left">
            <div class="higher">
                <p>对比分析</p>
                <el-button >单站点</el-button><el-button >多站点</el-button>
                    <el-date-picker
                    v-model="value1"
                    type="date"
                    class="date-picker"
                    placeholder="选择日期"
                    :picker-options="pickerOptions0">
                    </el-date-picker>
            </div>
            <div class="line"></div>
            <div class="search-content">
                <div v-for="result in searchResult" :key="result">
                    <div class="result">
                    <span>{{result}}</span>
                    
                    </div>
                </div>
            </div>
            <div class="line"></div>
            <div class="lower">
                <p>监测范围地图</p>  
                <BDmap></BDmap>
            </div>

      </div>
      <div class="right">
            <div class="chart"> <img src="../../assets/photo/1@1x.png"/></div>
            <div class="chart"> <img src="../../assets/photo/2@1x.png"/></div>
            <div class="chart"> <img src="../../assets/photo/3@1x.png"/></div>
            <div class="chart"> <img src="../../assets/photo/4@1x.png"/></div>
            <div class="chart"> <img src="../../assets/photo/5@1x.png"/></div>
            <div class="chart"> <img src="../../assets/photo/6@1x.png"/></div>            
      </div>
  </div>
</template>
<script>
import BDmap from '../common/map.vue'

export default {
    name:"analyse",
    data(){
      return {
        value1:"",
        pickerOptions0:"",
        searchResult: ['气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1', '气象仪1']
      }
    },
    methods: {   
  },
    components:{
    BDmap,
    }
  
}
</script>
<style scoped>
#analyse{
    position: absolute;
    top:48px;
    left: 96px;
    z-index: 1;
    background-color: #ffffff;
    height: 94.6%;
    width: 1250px;
}
img{
    width: 450px;
    height: 229px;
}
div{
    display: inline-block;
}

/*-----------左边  */
.left{
    width:208px;
    padding: 0 16px;
    height: 100%

}
p{
    font-size: 14px;
    color: #37403F;
    line-height: 32px;
}
.el-button{
    width: 98px;
    height: 32px;
}
.date-picker{
    padding:16px 0 0px;;
    width: 208px;
    border-bottom: 1px  #E3E6E5;
}
.line{
    background: #E3E6E5;
    height: 1px;
    width: 208px;
}

  .search-content {
    width: 208px;
    height: 70%;
    box-sizing: border-box;
    overflow: scroll;
    overflow-x: hidden
    /*background-color: aqua;*/
  }

  /* 滚动条 */
  .search-content::-webkit-scrollbar {
    width: 8px;
    height: 8px;
  }

  .search-content::-webkit-scrollbar-thumb {
    background-color: rgba(192, 192, 192, 1);
    border-radius: 0;
  }


  .result {
    width: 240px;
    height: 56px;
    padding: 25px 0 19px ;
    box-sizing: border-box;
    font-size: 12px;
    letter-spacing: 0;
    line-height: 12px;
  }

  .result:hover {
    background: rgba(174,230,138,0.15);
  }
  /*----- ditu --- */
  .lower{
    height: 17%;
     width: 240px;
     
  }
/*-----------、右边  */
.right{
    height: 100%;
    width: 1000px;
}
.chart{
    width: 490px;
    height: 100px;
}
</style>
