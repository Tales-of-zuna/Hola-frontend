<template>
  <v-sheet>
    <v-row
      ><v-col cols="12" md="4"
        ><v-img
          class="d-flex fill-height"
          src="https://d-themes.com/vue/riode/demo-24/images/home/banner/6.jpg"
          ><v-card color=" transparent" elevation="0">
            <v-card-title class="text-h6 text--secondary font-weight-regular">
              New collection
            </v-card-title>
            <v-card-subtitle class="text-h4 text--primary font-weight-bold">
              Buy 2, Get 1 Free* on everything
            </v-card-subtitle>
            <v-card-text class="">Must add 3 products to cart. </v-card-text>
            <v-card-actions>
              <v-btn color="white" class="text-subtitle-1" large light
                >text</v-btn
              >
            </v-card-actions>
          </v-card></v-img
        ></v-col
      >
      <v-col cols="12" md="8">
        <v-row
          ><v-col v-for="card in 6" :key="card" cols="6" md="4"
            ><v-card elevation="0">
              <v-img
                src="https://d-themes.com/vue/riode/server/uploads/demo_24_product_1_2_25839d064e.jpg"
              ></v-img>
              <p
                primary-title
                class="text--secondary text-subtitle-2 text-center"
              >
                iPhone 14 Pro MAX
              </p>
              <p class="mt-n4 text-subtitle-1 font-weight-bold text-center">
                1.500.000₮
              </p></v-card
            ></v-col
          ></v-row
        >
      </v-col></v-row
    >
  </v-sheet>
</template>

<script>
export default {};
</script>

<style></style>
