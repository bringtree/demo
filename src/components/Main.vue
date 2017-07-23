<template>
  <div class="main" id="main">
    <headerTool></headerTool>
    <Diagram></Diagram>
  </div>
</template>

<script>
  import Diagram from './common/diagram.vue'
  import headerTool from './common/headerTool.vue'

  export default {
    name: 'main',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        search: ""
      }
    },
    components: {
      Diagram,
      headerTool,
    },
    methods: {
      handleIconClick() {

      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .main {
    height: 100%;
  }

</style>
