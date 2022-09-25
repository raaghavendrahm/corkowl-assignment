<template>
  <div class="leftPane">
    <div class="leftPane-wrapper">
      <div class="leftPane-wrapper-flex-container">
        <div class="flex-item">
          <div class="icon">
            <font-awesome-icon :icon="['fas', 'desktop']" />
          </div>
          <p>Dashboard</p>
      </div>

        <div class="flex-item">
          <div class="icon">
            <font-awesome-icon :icon="['fas', 'layer-group']" />
          </div>
          <p>Inventory</p>
      </div>
        <div class="flex-item">
          <div class="icon">
            <font-awesome-icon :icon="['fas', 'shopping-bag']" />
          </div>
          <p>Orders</p>
      </div>
        <div class="flex-item">
          <div class="icon">
            <font-awesome-icon :icon="['fas', 'user-friends']" />
          </div>
          <p>Customers</p>
      </div>
        <div class="flex-item">
          <div class="icon">
            <font-awesome-icon :icon="['far', 'file-alt']" />
          </div>
          <p>Reports</p>
      </div>
        <div class="flex-item">
          <div class="icon">
            <font-awesome-icon :icon="['fas', 'dharmachakra']" />
          </div>
          <p>Settings</p>
      </div>

      <p class="footer-heading">CorkOwl</p>
      <p class="footer-sub-heading">
        &copy; 2022 CorkOwl, All Rights Reserved.
      </p>

      <div class="left-arrow">
        <font-awesome-icon :icon="['fas', 'arrow-circle-left']" />
      </div>

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "leftPane",
  }
</script>

<style>
  @import "./leftPane.css";
</style>