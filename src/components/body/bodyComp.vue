<template>
  <div class="bodyComp">
    <left-pane />
  </div>
</template>

<script>
  import leftPane from "../leftPane/leftPane.vue";

  export default {
    name: "bodyComp",
    components: {
      leftPane
    }
  }
</script>

<style>
  @import "./bodyComp.css";
</style>