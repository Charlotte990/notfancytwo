<template>
  <div>
    <div class="heading">
      <p>Random Number Generator</p>
    </div>
    <el-selection-bar></el-selection-bar>
  </div>
</template>

<script>
import SelectionBar from './SelectionBar'

export default {
  components: {
    'ElSelectionBar': SelectionBar
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.heading {
  font-size: 3em;
  padding: 1em;
}
p {
  margin: 0;
}
</style>
