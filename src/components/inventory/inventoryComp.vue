<template>
  <div class="inventory">
    <p>Inventory</p>
    <div class="product-list">
      <div class="product-list-nav">
        <input type="checkbox" id="checkbox" />
        <div>PRODUCT</div>
        <div>RATING</div>
        <div>VINTAGE</div>
        <div>QTY</div>
        <div>VOLUME</div>
        <div>COST</div>
        <div>PRICE</div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "inventoryComp",
  }
</script>

<style>
  @import"./inventoryComp.css";
</style>