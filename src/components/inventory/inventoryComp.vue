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

      <div class="products" v-for="(product, index) in products" :key="index">
        <product-comp :product="product"/>
      </div>

    </div>
  </div>
</template>

<script>
  import productComp from "../product/productComp.vue";

  export default {
    name: "inventoryComp",
    components: {
      productComp,
    },

    data() {
      return {
        products: [
          {
            "name": {
              "heading": "Staglin Family Vineyard Red Wine",
              "subHeading": "France · Sauternes",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "1950's",
            "qty": "04",
            "volume": "Standard (750 mL)",
            "cost": "$56.95",
            "price": "$56.95",
            "insidePartOne": {
              "name": "Staglin Family Vineyard Red Wine",
              "region": "France · Sauternes",
              "vintage": "1950's",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },

          {
            "name": {
              "heading": "Bibi Graetz Testamatta Tos Wine",
              "subHeading": "Chianti · Blends and Other",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "2015",
            "qty": "32",
            "volume": "Magnum (1500 mL)",
            "cost": "$71.95",
            "price": "$72.95",
            "insidePartOne": {
              "name": "Bibi Graetz Testamatta Tos Wine",
              "region": "Chianti · Blends and Other",
              "vintage": "2015",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },

          {
            "name": {
              "heading": "Cayuse Syrah en Chamber Wine",
              "subHeading": "Syrah",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "2012",
            "qty": "12",
            "volume": "Standard (750 mL)",
            "cost": "$139.95",
            "price": "$150.00",
            "insidePartOne": {
              "name": "Cayuse Syrah en Chamber Wine",
              "region": "Syrah",
              "vintage": "2012",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },

          {
            "name": {
              "heading": "Staglin Family Vineyard INEO Red Wine",
              "subHeading": "United States · California · Blends",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "2010",
            "qty": "04",
            "volume": "Odd Ball (5000 mL)",
            "cost": "$56.95",
            "price": "$56.95",
            "insidePartOne": {
              "name": "Staglin Family Vineyard INEO Red Wine",
              "region": "United States · California · Blends",
              "vintage": "2010",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },

          {
            "name": {
              "heading": "K Vintners Syrah Cattle king",
              "subHeading": "France · Sauternes",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "2015",
            "qty": "25",
            "volume": "Magnum (1500 mL)",
            "cost": "$79.95",
            "price": "$92.95",
            "insidePartOne": {
              "name": "K Vintners Syrah Cattle king",
              "region": "France · Sauternes",
              "vintage": "2015",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },

          {
            "name": {
              "heading": "L'Ecole No. 41 Ferguson",
              "subHeading": "United state · Celifornia · Blends",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "2004",
            "qty": "04",
            "volume": "Magnum (1500 mL)",
            "cost": "$54.95",
            "price": "$59.95",
            "insidePartOne": {
              "name": "L'Ecole No. 41 Ferguson",
              "region": "United state · Celifornia · Blends",
              "vintage": "2004",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },

          {
            "name": {
              "heading": "Staglin Family Vineyard Red Wine",
              "subHeading": "France · Sauternes",
            },
            "rating": {
              "partOne": "RP 95",
              "partTwo": "+3",
            },
            "vintage": "1950's",
            "qty": "22",
            "volume": "Regular (750 mL)",
            "cost": "$56.95",
            "price": "$59.95",
            "insidePartOne": {
              "name": "Staglin Family Vineyard Red Wine",
              "region": "France · Sauternes",
              "vintage": "1950's",
            },
            "insidePartTwo": {
              "rating": {
                "rating1": {
                  "name": "James Suckling's",
                  "rating": "JS 95"
                },
                "rating2": {
                  "name": "Robert Parker",
                  "rating": "RP 80"
                },
                "rating3": {
                  "name": "Antonio Galloni’s",
                  "rating": "---"
                },
                "rating4": {
                  "name": "Wine Spectator Tasting",
                  "rating": "WS 79"
                }
              },

              "stock": {
                "stock1": {
                  "name": "Possimus",
                  "units": "43 units"
                },
                "stock2": {
                  "name": "Downtown Condo",
                  "units": "95 units"
                },
              } 
            }
          },
        
        ]
      }
    }
  }
</script>

<style>
  @import"./inventoryComp.css";
</style>