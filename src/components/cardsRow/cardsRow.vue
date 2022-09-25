<template>
  <div class="cards-row">
    <card-comp :cardType="'openOrders'" :cardTitle="' Open Orders'" :cardNumber="'239'"/>
    <card-comp :cardType="'transitOrders'" :cardTitle="'Orders in Transit'" :cardNumber="'126'"/>
    <card-comp :cardType="'fullfilledOrders'" :cardTitle="'Fullfilled Orders'" :cardNumber="'1,254'"/>
    <card-comp :cardType="'cancelledOrders'" :cardTitle="'Cancelled Orders'" :cardNumber="'35'"/>
  </div>
</template>

<script>
  import cardComp from "../card/cardComp.vue";
  export default {
    name: "cardsRow",
    components: {
      cardComp,
    }
  }
</script>

<style>
  @import './cardsRow.css';
</style>