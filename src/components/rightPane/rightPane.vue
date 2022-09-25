<template>
  <div class="right-pane">
    <overview-comp />
    <cards-row />
    <sales-comp />
    <inventory-comp />
  </div>
</template>

<script>
  import overviewComp from "../overview/overviewComp.vue";
  import cardsRow from "../cardsRow/cardsRow.vue";
  import salesComp from "../sales/salesComp.vue";
  import inventoryComp from "../inventory/inventoryComp.vue";

  export default {
    name: "rightPane",
    components: {
      overviewComp,
      cardsRow,
      salesComp,
      inventoryComp
    }
  }
</script>

<style>
  @import "./rightPane.css";
</style>