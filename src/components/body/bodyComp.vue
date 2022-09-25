<template>
  <div class="bodyComp">
    <left-pane />
    <right-pane />
  </div>
</template>

<script>
  import leftPane from "../leftPane/leftPane.vue";
  import rightPane from "../rightPane/rightPane.vue";

  export default {
    name: "bodyComp",
    components: {
      leftPane,
      rightPane
    }
  }
</script>

<style>
  @import "./bodyComp.css";
</style>