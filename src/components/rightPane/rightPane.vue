<template>
  <div class="right-pane">
    <overview-comp />
    <cards-row />
  </div>
</template>

<script>
  import overviewComp from "../overview/overviewComp.vue";
  import cardsRow from "../cardsRow/cardsRow.vue";

  export default {
    name: "rightPane",
    components: {
      overviewComp,
      cardsRow
    }
  }
</script>

<style>
  @import "./rightPane.css";
</style>