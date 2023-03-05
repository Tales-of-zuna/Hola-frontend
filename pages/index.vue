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
        <categories />
        <v-divider class="my-16"></v-divider>

        <v-sheet class="my-16">
          <p class="text-center text-h4 font-weight-bold">Best sellers</p>
          <bestseller /> </v-sheet
        ><v-divider class="my-16"></v-divider>

        <v-sheet class="my-16">
          <p class="text-center text-h4 font-weight-bold">Featured</p>
          <featured />
        </v-sheet>
        <v-divider class="my-16"></v-divider>
        <v-sheet class="my-16">
          <p class="text-center text-h4 font-weight-bold">
            Product request ideas
          </p>
          <v-row
            ><v-col cols="12" md="6"
              ><v-sheet class="d-flex fill-height justify-center align-center"
                ><v-expansion-panels tile class="fill-height" inset>
                  <v-expansion-panel v-for="(item, i) in 5" :key="i">
                    <v-expansion-panel-header
                      ><v-sheet
                        class="text-h6 d-flex align-center text--secondary"
                        >What is that<v-icon class="ml-3">
                          mdi-amplifier</v-icon
                        ></v-sheet
                      >
                    </v-expansion-panel-header>
                    <v-expansion-panel-content class="text--secondary">
                      Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                      sed do eiusmod tempor incididunt ut labore et dolore magna
                      aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                      ullamco laboris nisi ut aliquip ex ea commodo consequat.
                    </v-expansion-panel-content>
                  </v-expansion-panel>
                </v-expansion-panels></v-sheet
              ></v-col
            ><v-col cols="12" md="6"
              ><v-img
                src="https://img.freepik.com/free-psd/beige-product-backdrop-mockup-psd-with-shadow_53876-141761.jpg?w=1380&t=st=1678023211~exp=1678023811~hmac=0b276733ac7f8871633cac0ea53362db82958dd333468df4faf8a467a918b5ba"
                ><v-sheet
                  class="d-flex fill-height justify-center align-center"
                  color="transparent"
                  ><v-card color=" transparent " elevation="0">
                    <p class="text-h4 text-center font-weight-bold">
                      Product request
                    </p>
                    <p
                      class="mt-n5 text-h6 text-center font-weight-regular text--secondary"
                    >
                      Start Shopping Right Now
                    </p>
                    <v-text-field
                      label="Your phone number"
                      placeholder="89007861"
                      filled
                      rounded
                      dense
                      color="grey darken-3"
                    ></v-text-field>
                    <v-textarea
                      outlined
                      color="darken-3 grey"
                      name="input-7-4"
                      label="Your product idea"
                    ></v-textarea>
                    <v-card-actions>
                      <v-btn color="white" block>Send request</v-btn>
                    </v-card-actions>
                  </v-card></v-sheet
                ></v-img
              ></v-col
            ></v-row
          >
        </v-sheet></v-col
      ></v-row
    >
  </v-container>
</template>

<script>
import Bestseller from "../components/home/bestseller.vue";
import Categories from "../components/home/categories.vue";
import Featured from "../components/home/featured.vue";
import Topbanner from "../components/home/topbanner.vue";

export default {
  name: "IndexPage",
  components: { Topbanner, Categories, Bestseller, Featured },
};
</script>
<style>
.zuna {
  height: 100vh;
}
</style>
