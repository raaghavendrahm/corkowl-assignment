<template>
  <div class="right-pane">
    <overview-comp />
  </div>
</template>

<script>
  import overviewComp from "../overview/overviewComp.vue";

  export default {
    name: "rightPane",
    components: {
      overviewComp
    }
  }
</script>

<style>
  @import "./rightPane.css";
</style>