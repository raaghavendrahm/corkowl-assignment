<template>
  <div class="sales">
    <p>Sales detail</p>
    <div class="total-sales-overview">
      <div class="sales-nav">
        <div class="heading-and-date">
          <p class="heading">Total Sales Overview</p>
          <p class="date">7 - 13 Aug, 2020</p>
        </div>
        <div class="refresh-metrics">
          <div class="icon">
            <font-awesome-icon :icon="['fas', 'sync']" />
          </div>
          <p>Refresh Metrics</p>
        </div>
        <div class="filter">
          <div>Filter by</div>
          <div>|</div>
          <div>This week</div>
          <div class="down-arrow">
            <font-awesome-icon :icon="['fas', 'chevron-down']" />
          </div>
        </div>
      </div>
      <div class="horizontal-line"></div>
      <div class="sales-details">
        <div class="sales-left-pane">
          <div class="left-top-flex">
            <div class="black-green-line">
              <div>${{ dataFromAPI.salesAmount }}</div>
              <div class="green-line">
                <div class="icon">
                  <font-awesome-icon :icon="['fas', 'chart-line']" />
                </div>
                <div>+{{ dataFromAPI.percentageSalesRaise }}% from last week</div>
              </div>
            </div>

            <div class="green-black-line">
              <div class="icon">
                <font-awesome-icon :icon="['fas', 'chart-line']" />
              </div>
              <div>Highest revenue since 2 weeks ago</div>
            </div>
          </div>

          <div class="line-chart">
            <div class="inner-div">
              <!-- <LineChart /> -->
            </div>
          </div>
        </div>
        <div class="sales-right-pane">
          <div>Total Profit</div>
          <div>${{ dataFromAPI.totalProfit }}</div>
          <div class="green-line">
            <div class="icon">
              <font-awesome-icon :icon="['fas', 'chart-line']" />
            </div>
            <div>+{{ dataFromAPI.percentageProfitRaise }}% from last week</div>
          </div>
          <div>Total Products Sold</div>
          <div>{{ dataFromAPI.totalProductsSold }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "salesComp",
    data() {
      return {
        dataFromAPI: {
          salesAmount: '74,729.00',
          percentageSalesRaise: '21',
          totalProfit: '12,545.00',
          percentageProfitRaise: '23',
          totalProductsSold: '329'
        }
      }
    }
  }
</script>

<style>
  @import "./salesComp.css";
</style>