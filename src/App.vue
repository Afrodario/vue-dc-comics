<template>
  <div id="app">
    <DcHeader/>
    <DcMain/>
    <DcFooter/>
  </div>
</template>

<script>
import DcHeader from './components/DcHeader.vue'
import DcMain from './components/DcMain.vue'
import DcFooter from './components/DcFooter.vue'

export default {
  name: 'App',
  components: {
    DcHeader,
    DcMain,
    DcFooter,
  }
}
</script>

<style lang="scss">
  @import "./assets/style/common.scss";
</style>
