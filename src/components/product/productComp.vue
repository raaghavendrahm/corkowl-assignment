<template>
    <div class="border" :class="borderStyle">
      <div class="product">
        <input type="checkbox" />
        <div class="img-name">
          <img src="../../assets/Wine.png" alt="Wine" />
          <div class="wine-name">
            <p class="heading">{{ product.name.heading }}</p>
            <p class="sub-heading">{{ product.name.subHeading }}</p>
          </div>
        </div>
        <div class="rating">
          <div>{{ product.rating.partOne }}</div>
          <div>{{ product.rating.partTwo }}</div>
        </div>
        <div class="vintage">{{ product.vintage }}</div>
        <div class="qty">{{ product.qty }}</div>
        <div class="volume">{{ product.volume }}</div>
        <div class="cost">{{ product.cost }}</div>
        <div class="price">{{ product.price }}</div>

        <!-- Displayed only when the product is collapsed -->
        <div class="down-arrow" @click="toggleExpand" v-if="!isExpanded" >
          <font-awesome-icon :icon="['fas', 'chevron-down']" />
        </div>

        <!-- Displayed only when the product is expanded  -->
        <div class="up-arrow" @click="toggleExpand" v-if="isExpanded">
            <font-awesome-icon :icon="['fas', 'chevron-up']" />
        </div>
      </div>

      <!-- Toggle Dropdown-->
      <div class="content" v-if="isExpanded">
        <div class="content-nav">
          <div class="heading-flex">
            <div class="heading">{{ product.insidePartOne.name }}</div>
            <div class="sub-heading">
              <span class="bold">Region: </span>
              <span class="light">{{ product.insidePartOne.region }}</span>
            </div>
          </div>
          <div class="vintage">
            <span class="bold">Vintage: </span>
            <span class="light">{{ product.insidePartOne.vintage }}</span>
          </div>
          <div class="view-wine">
            <u>View wine</u>
          </div>
          <div class="edit-icon">
            <font-awesome-icon :icon="['far', 'edit']" />
          </div>
          <div class="delete-icon">
            <font-awesome-icon :icon="['far', 'trash-alt']" />
          </div>
        </div>
        <div class="horizontal-line"></div>
        <div class="content-body">
          <div class="left">
            <div class="rating">Rating</div>
            <div class="left-flex">
              <div class="name-and-code nc-1">
                <div class="name">{{ product.insidePartTwo.rating.rating1.name }}</div>
                <div class="code">{{ product.insidePartTwo.rating.rating1.rating }}</div>
              </div>
              <div class="name-and-code nc-2">
                <div class="name">{{ product.insidePartTwo.rating.rating2.name }}</div>
                <div class="code">{{ product.insidePartTwo.rating.rating2.rating }}</div>
              </div>
              <div class="name-and-code nc-3">
                <div class="name">{{ product.insidePartTwo.rating.rating3.name }}</div>
                <div class="code">{{ product.insidePartTwo.rating.rating3.rating }}</div>
              </div>
              <div class="name-and-code nc-4">
                <div class="name">{{ product.insidePartTwo.rating.rating4.name }}</div>
                <div class="code">{{ product.insidePartTwo.rating.rating4.rating }}</div>
              </div>
            </div>
          </div>
          <div class="right">
            <div class="stock">Stock</div>
            <div class="right-flex">
              <div class="name-and-code nc-1">
                <div class="name">{{ product.insidePartTwo.stock.stock1.name }}</div>
                <div class="code">{{ product.insidePartTwo.stock.stock1.units }}</div>
              </div>
              <div class="name-and-code nc-2">
                <div class="name">{{ product.insidePartTwo.stock.stock2.name }}</div>
                <div class="code">{{ product.insidePartTwo.stock.stock2.units }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: "productComp",
    data() {
      return {
        isExpanded: false,
        isDisplayed: false,
      }
    },
    props: {
      product: Object,
    },
    methods: {
      toggleExpand() {
        this.isExpanded = !this.isExpanded;
      },
      toggleDisplay() {
        this.isDisplayed = !this.isDisplayed
      }
    },
    computed: {
      borderStyle() {
        if (this.isExpanded) {
          return 'expandedBorderClass';
        } else {
          return '';
        }
      },
      displayDown() {
        if (this.isExpanded) {
          return 'expandedBorderClass';
        } else {
          return '';
        }
      },      
    }
  }
</script>

<style scoped>
  @import "./productComp.css";
  .expandedBorderClass {
    border-left: 1px solid #ecf1f4;
    border-right: 1px solid #ecf1f4;
    border-bottom: 1px solid #ecf1f4;
  }
  
</style>