<template>
  <div class="overview">
    <p>Overview</p>
      <button class="add">
        <div class="icon">
          <font-awesome-icon :icon="['fas', 'plus-circle']" />
        </div>
        <p>ADD NEW WINE</p>
      </button>
  </div>
</template>

<script>
  export default {
    name: "overviewComp",
  }
</script>

<style>
  @import "./overviewComp.css";
</style>