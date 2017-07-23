<template>
  <div class="main" id="main">
      <headerTool></headerTool>
      <div class="BDmap">
        <BDmap></BDmap>
      </div>
      <router-view></router-view>
       <Diagram></Diagram>
  </div>
</template>

<script>
import Diagram from './common/diagram.vue'
import BDmap from './common/map.vue'
import headerTool from './common/headerTool.vue'

export default {
  name: 'fireSciencManagement',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      search:""
    }
  },
  components:{
    Diagram,
    BDmap,
    headerTool,
  },
  methods:{
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main{
    height:100%;
}
.BDmap{
    height:94.8%;
}

</style>
