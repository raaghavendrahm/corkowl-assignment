<template>
  <div class="right-pane">
    <overview-comp />
    <cards-row />
    <sales-comp />
  </div>
</template>

<script>
  import overviewComp from "../overview/overviewComp.vue";
  import cardsRow from "../cardsRow/cardsRow.vue";
  import salesComp from "../sales/salesComp.vue";

  export default {
    name: "rightPane",
    components: {
      overviewComp,
      cardsRow,
      salesComp
    }
  }
</script>

<style>
  @import "./rightPane.css";
</style>