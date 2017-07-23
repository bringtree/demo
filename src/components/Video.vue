<template>
  <div class="monitor">
    <headerTool></headerTool>
    <div class="BDmap">
      <mapPlane></mapPlane>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
  import headerTool from './common/headerTool.vue'
  import monintorNav from './common/monintorNav.vue'
  import mapPlane from './video/mapPlane.vue'

  export default {
    name: 'monitor',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        search: "",
        activeIndex2: ""
      }
    },
    components: {
      headerTool,
      monintorNav,
      mapPlane,
    },
    methods: {}
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .monitor {
    height: 100%;
  }

  .BDmap {
    height: 94.8%;
  }
</style>
