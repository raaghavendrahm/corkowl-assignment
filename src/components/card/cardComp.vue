<template>
  <div class="card" :class="cardColor">
    <div class="info">
      <p>{{ cardTitle }}</p>
      <p>{{ cardNumber }}</p>
    </div>
    <div class="icon" :class="iconColor">
      <font-awesome-icon :icon="iconType" />
    </div>
  </div>
</template>

<script>
  export default {
    name: "cardComp",
    props: {
      cardType: {
        type: String,
      },
      cardTitle: {
        type: String,
      },
      cardNumber: {
        type: String,
      }
    },
    computed: {
      cardColor() {
        if (this.cardType === "openOrders") {
          return "card-orange";
        } else if (this.cardType === "transitOrders") {
          return "card-blue";
        } else if (this.cardType === "fullfilledOrders") {
          return "card-green";
        } else if (this.cardType === "cancelledOrders") {
          return "card-red";
        } else {
          return "card-gray";
        }
      },
      iconColor() {
        if (this.cardType === "openOrders") {
          return "icon-orange";
        } else if (this.cardType === "transitOrders") {
          return "icon-blue";
        } else if (this.cardType === "fullfilledOrders") {
          return "icon-green";
        } else if (this.cardType === "cancelledOrders") {
          return "icon-red";
        } else {
          return "icon-gray";
        }
      },
      iconType() {
        if (this.cardType === "openOrders") {
          return ['fas', 'shopping-basket'];
        } else if (this.cardType === "transitOrders") {
          return ['fas', 'truck'];
        } else if (this.cardType === "fullfilledOrders") {
          return ['fas', 'store'];
        } else if (this.cardType === "cancelledOrders") {
          return ['far', 'times-circle'];
        } else {
          return ['fab', 'vuejs'];
        }
      }
    }
  }
</script>

<style>
  @import "./cardComp.css";
</style>
 