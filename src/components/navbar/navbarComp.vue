<template>
  <div class="navbar">
      <!-- LEFT-NAV -->
      <div class="nav-left">
        <p>CORKOWL</p>
      </div>

      <!-- MID-NAV -->
      <div class="nav-mid">
        <div class="nav-mid-wrapper">
          <div class="nav-mid-wrapper-flex-container">
            <form class="search-form">
              <div class="searchbox-wrapper">
                <button type="submit" class="searchbox-submit" @click="searchWine">
                  <div class="search-icon">
                    <font-awesome-icon :icon="['fas', 'search']" />
                  </div>
                </button>
                <input
                  id="inputField"
                  type="search"
                  placeholder="Search wines, customers here..."
                  style="padding-right: 5px;"
                />
              </div>
            </form>
          </div>
        </div>
        <div class="bell-icon">
          <font-awesome-icon :icon="['far', 'bell']" />
        </div>
      </div>

      <!-- RIGHT-NAV -->
      <div class="nav-right">
        <div class="nav-right-wrapper">
          <div class="nav-right-wrapper-flex-container">
            <p class="username">{{ this.dataFromAPI.name }}</p>
            <div class="user-avatar">
              <img src="../../assets/tejaswi.jpg" alt="boss" />
            </div>
            <div class="dropDown">
              <div class="down-arrow" v-if="!isDropdownExpanded" @click="toggleExpansion">
                <font-awesome-icon :icon="['fas', 'angle-down']" />
              </div>
              <div class="up-arrow" v-if="isDropdownExpanded" @click="toggleExpansion">
                <font-awesome-icon :icon="['fas', 'angle-up']" />
              </div>
              <div class="sign-out" v-if="isDropdownExpanded">
                <div class="my-account">
                  <u>My Account</u>
                </div>
                <button>Sign Out</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: "navbarComp",
    data(){
      return {
        dataFromAPI: {
          name: 'P. Tejaswi',
        },
        isDropdownExpanded: false,
      }
    },

    methods: {
      // To empty the input field on clicking search:
      searchWine(e) {
        e.preventDefault();
        document.getElementById("inputField").value = '';
      },

      // To toggle the sign out dropdwon:
      toggleExpansion() {
        this.isDropdownExpanded = !this.isDropdownExpanded;
      }
    }
  }
</script>

<style scoped>
 @import "./navbarComp.css";
</style>