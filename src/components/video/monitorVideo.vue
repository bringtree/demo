<template>
  <div class="monitorVideo">
    <div class="left">
        <div class="higher">
            <p>监测站视频</p>
            <el-select v-model="value" placeholder="请选择" class="monitorVideo-sel">
              <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value">
              </el-option>
            </el-select>
        </div>
        <div class="search-line"></div>
        <div class="search-content">
          <div v-for="result in searchResult" :key="result">
            <div class="result">
              <span>01</span>&nbsp&nbsp&nbsp
              <span>{{result}}</span>
              
              </div>
          </div>
        </div>
    </div>
    <div class="right">
        <img src="../../assets/photo/视频监测画面@1x.png">
    </div>
  </div>  
</template>

<script type="text/ecmascript-6">
  export default {
    name:"monitorVideo",
    data () {
      return {
        options: [{
          value: '选项1',
          label: '站点1'
        }, {
          value: '选项2',
          label: '站点1'
        }, {
          value: '选项3',
          label: '站点1'
        }, {
          value: '选项4',
          label: '站点1'
        }, {
          value: '选项5',
          label: '站点1'
        }],
        value: '',
        keyword: '',
        rowResult: ['二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光'],
        searchResult: ['二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光', '二井湾HQ202光电跟踪仪白光']
      }
    },
    methods: {
      search () {
        var result = []
        for (var i = 0; i < this.rowResult.length; i++) {
          if (this.rowResult[i].indexOf(this.keyword) >= 0) {
            result.push(this.rowResult[i])
          }
        }
        this.searchResult = result
      }
    }
  }

</script>

<style scoped>
  .monitorVideo {
    height: 94%;
    width: 100%;
    box-sizing: border-box;
    position: absolute;
    top:48px;
    left: 96px;
    color: #ffffff;
  }
  div{
    display: inline-block;
  }
  /*----------  */
  .left{
    width: 240px;
    height: 100%;
    float: left;
    box-sizing: border-box;
    background-color: #454D4C;
  }
  .higher{
    height: 10%;

  }
  p{
      font-size: 14px;
      line-height: 32px;
      padding:0 15px;
  }

.monitorVideo-sel{
  padding-left:12px; 
  width: 216px;
}

  .search-content {
    width: 240px;
    height: 87%;
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

  
  .search-line {
    height: 12px;
    margin: 0 12px;
    border-bottom: 1px solid #D9D9D9;
  }

  .result {
    width: 240px;
    height: 56px;
    padding: 25px 15px 19px 15px;
    box-sizing: border-box;
    font-size: 12px;
    letter-spacing: 0;
    line-height: 12px;
    background-color: #454D4C;
  }

  .result:hover {
    background: #5EBF1D;
  }
  /*---------右边  */
  .right{
    float: left;
    width:80%;
    overflow: hidden;
 }
  img{
        height: 100%;
        width: 100%
  }
</style>
