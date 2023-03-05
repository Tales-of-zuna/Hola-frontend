<template>
  <v-container grid-list-xs>
    <v-row justify-md="center"
      ><v-col cols="12" md="8"
        ><Topbanner /> <v-divider class="my-16"></v-divider>
        <v-sheet class="my-16">
          <p class="text-center text-h4 font-weight-bold">End of Summer Sale</p>
          <p class="text-center font-weight-light">
            Get 30% off full price and sale items, with promo code SPORT30
            through 9/3. Exclusions apply
          </p>
          <div class="d-flex justify-center">
            <v-btn large class="mx-2" color="grey darken-3" dark tile
              >Mobile phones <v-icon>mdi-chevron-right</v-icon></v-btn
            ><v-btn large class="mx-2" color="grey darken-3" dark tile
              >Consoles <v-icon>mdi-chevron-right</v-icon></v-btn
            >
          </div>
        </v-sheet>
        <categories /> </v-col
    ></v-row>
  </v-container>
</template>

<script>
import Categories from "../components/home/categories.vue";
import Topbanner from "../components/home/topbanner.vue";

export default {
  name: "IndexPage",
  components: { Topbanner, Categories },
};
</script>
<style>
.zuna {
  height: 100vh;
}
</style>
