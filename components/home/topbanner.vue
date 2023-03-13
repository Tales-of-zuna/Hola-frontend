<template>
  <v-sheet>
    <v-row>
      <v-col cols="12" md="8"
        ><v-carousel
          cycle
          show-arrows-on-hover
          hide-delimiter-background
          delimiter-icon="mdi-minus"
        >
          <v-carousel-item
            src="https://d-themes.com/vue/riode/demo-24/img/1.8ccd473.jpg"
          >
            <v-container grid-list-xs>
              <v-row fill-height
                ><v-col cols="12" class="d-flex justify-end align-center"
                  ><v-sheet
                    color="transparent"
                    elevation="0"
                    height="450"
                    class="d-flex align-center"
                  >
                    <v-card color="transparent" elevation="0">
                      <v-card-text
                        class="text-regular text-right font-weight-bold"
                        >BEST SELLERS
                      </v-card-text>
                      <v-card-subtitle
                        class="text-h3 font-weight-bold mt-n5 text-right"
                      >
                        Galaxy Z fold 4
                      </v-card-subtitle>
                      <v-card-subtitle class="text-right mt-n5"
                        >Free shipping on all over 99$
                      </v-card-subtitle>

                      <v-card-actions>
                        <v-hover v-slot="{ hover }"
                          ><v-btn
                            block
                            color="white"
                            class="font-weight-bold"
                            tile
                            :elevation="hover ? 5 : 0"
                            >View more</v-btn
                          ></v-hover
                        >
                      </v-card-actions>
                    </v-card>
                  </v-sheet></v-col
                ></v-row
              >
            </v-container> </v-carousel-item
          ><v-carousel-item
            src="https://d-themes.com/vue/riode/demo-24/img/2.1d9fc26.jpg"
            ><v-container grid-list-xs>
              <v-row fill-height
                ><v-col cols="12" class="d-flex align-center"
                  ><v-sheet
                    color="transparent"
                    elevation="0"
                    height="450"
                    class="d-flex align-center"
                  >
                    <v-card color="transparent" elevation="0">
                      <v-card-text class="text-regular font-weight-bold"
                        >BEST SELLERS
                      </v-card-text>
                      <v-card-subtitle class="text-h3 font-weight-bold mt-n5">
                        iPhone 14
                      </v-card-subtitle>
                      <v-card-subtitle class="mt-n5"
                        >Free shipping on all over 99$
                      </v-card-subtitle>

                      <v-card-actions>
                        <v-btn
                          block
                          color="white"
                          class="font-weight-bold"
                          tile
                          elevation="0"
                          >View more</v-btn
                        >
                      </v-card-actions>
                    </v-card>
                  </v-sheet></v-col
                ></v-row
              >
            </v-container></v-carousel-item
          ></v-carousel
        ></v-col
      >
      <v-col cols="12" md="4"
        ><v-img
          class="d-flex justify-center align-center"
          height="500"
          src="https://d-themes.com/vue/riode/demo-24/img/1.b8991a5.jpg"
          ><v-card color=" transparent" elevation="0" dark>
            <p class="text-h6 font-weight-regular text-center">
              New collection
            </p>
            <p class="text-h4 font-weight-bold text-center">
              Buy 2, Get 1 Free* on everything
            </p>
            <v-card-subtitle class="text-center"
              >Must add 3 products to cart.
            </v-card-subtitle>
          </v-card></v-img
        ></v-col
      ></v-row
    >
  </v-sheet>
</template>

<script>
export default {};
</script>

<style></style>
