<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" fixed temporary>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-container grid-list-xs>
      <v-row class="d-flex justify-center"
        ><v-col cols="12" md="8"></v-col
      ></v-row>
    </v-container>
    <v-app-bar
      fixed
      app
      color="white"
      elevation="5"
      elevate-on-scroll
      height="90"
    >
      <v-container grid-list-xs>
        <v-row justify="center"
          ><v-col class="d-flex align-center" cols="12" md="8"
            ><v-app-bar-nav-icon
              class="d-flex d-md-none"
              @click.stop="drawer = !drawer"
            />

            <v-toolbar-title
              ><v-img
                width="150"
                src="https://d-themes.com/vue/riode/demo-24/img/logo.3092498.png"
              ></v-img
            ></v-toolbar-title>
            <v-spacer />
            <div class="d-none d-md-flex">
              <v-btn small to="/" color="grey darken-3" plain>Нүүр</v-btn>
              <v-menu open-on-hover bottom offset-y>
                <template v-slot:activator="{ on, attrs }">
                  <v-btn
                    color="grey darken-3"
                    small
                    text
                    v-bind="attrs"
                    v-on="on"
                  >
                    ангилал<v-icon>mdi-chevron-down</v-icon>
                  </v-btn>
                </template>

                <v-list>
                  <v-list-item
                    to="/abudabi"
                    class="font-weight-regular text--secondary"
                    v-for="i in categories"
                    :key="i"
                  >
                    {{ i.name }} <v-spacer></v-spacer>
                    <v-icon>mdi-chevron-right</v-icon>
                  </v-list-item>
                </v-list>
              </v-menu>
              <v-menu open-on-hover bottom offset-y>
                <template v-slot:activator="{ on, attrs }">
                  <v-btn
                    color="grey darken-3"
                    small
                    text
                    v-bind="attrs"
                    v-on="on"
                  >
                    Бүтээгдэхүүн<v-icon>mdi-chevron-down</v-icon>
                  </v-btn>
                </template>
                <v-sheet class="d-flex" color="white"
                  ><v-list>
                    <v-list-item
                      ><v-list-item-content>
                        <v-list-item-title class="font-weight-bold"
                          >Гар утас</v-list-item-title
                        >
                      </v-list-item-content></v-list-item
                    >
                    <v-list-item
                      v-for="phone in productphone"
                      :key="phone"
                      :to="phone.link"
                    >
                      <v-list-item-content>
                        <v-list-item-title
                          class="text-subtitle-2 text--secondary font-weight-regular"
                          >{{ phone.name }}</v-list-item-title
                        >
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                  <v-list>
                    <v-list-item
                      ><v-list-item-content>
                        <v-list-item-title class="font-weight-bold"
                          >Consoles</v-list-item-title
                        >
                      </v-list-item-content></v-list-item
                    >
                    <v-list-item v-for="phone in 5" :key="phone" to="/as ">
                      <v-list-item-content>
                        <v-list-item-title
                          class="text-subtitle-2 text--secondary font-weight-regular"
                          >Samsung Galaxy Fold 4</v-list-item-title
                        >
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                  <v-img
                    class="d-flex justify-center align-end ml-1"
                    width="200"
                    src="https://d-themes.com/vue/riode/demo-24/images/menu/banner-2.jpg"
                    ><v-sheet
                      elevation="0"
                      dark
                      color="transparent"
                      class="pb-2"
                    >
                      <div>
                        <p class="font-weight-bold text-h4 text-center">Sale</p>
                        <p class="mt-n5 text-center">100$-200$</p>
                      </div>

                      <div class="d-flex justify-center">
                        <v-btn
                          color="transparent"
                          class="text-subtitle2 text-center"
                          >Details <v-icon>mdi-chevron-right </v-icon></v-btn
                        >
                      </div>
                    </v-sheet></v-img
                  ></v-sheet
                > </v-menu
              ><v-menu open-on-hover bottom offset-y>
                <template v-slot:activator="{ on, attrs }">
                  <v-btn
                    color="grey darken-3"
                    small
                    text
                    v-bind="attrs"
                    v-on="on"
                  >
                    Ашигласан<v-icon>mdi-chevron-down</v-icon>
                  </v-btn>
                </template>

                <v-sheet class="d-flex" color="white"
                  ><v-list color="">
                    <v-list-item
                      ><v-list-item-content>
                        <v-list-item-title class="font-weight-bold"
                          >Mobile Phones</v-list-item-title
                        >
                      </v-list-item-content></v-list-item
                    >
                    <v-list-item v-for="phone in 5" :key="phone" to="/as">
                      <v-list-item-content>
                        <v-list-item-title
                          class="text-subtitle-2 text--secondary font-weight-regular"
                          >Samsung Galaxy Fold 4</v-list-item-title
                        >
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                  <v-list>
                    <v-list-item
                      ><v-list-item-content>
                        <v-list-item-title class="font-weight-bold"
                          >Consoles</v-list-item-title
                        >
                      </v-list-item-content></v-list-item
                    >
                    <v-list-item v-for="phone in 5" :key="phone" to="/as ">
                      <v-list-item-content>
                        <v-list-item-title
                          class="text-subtitle-2 text--secondary font-weight-regular"
                          >Samsung Galaxy Fold 4</v-list-item-title
                        >
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                  <v-img
                    class="d-flex justify-center align-end ml-1"
                    width="200"
                    src="https://d-themes.com/vue/riode/demo-24/images/menu/banner-1.jpg"
                    ><v-sheet elevation="0" color="transparent" class="pb-2">
                      <div>
                        <p class="font-weight-bold text-h4 text-center">
                          Used Products
                        </p>
                        <p class="mt-n5 text-center">100$-200$</p>
                      </div>

                      <div class="d-flex justify-center">
                        <v-btn
                          color="transparent"
                          class="text-subtitle2 text-center"
                          >Details <v-icon>mdi-chevron-right </v-icon></v-btn
                        >
                      </div>
                    </v-sheet></v-img
                  ></v-sheet
                >
              </v-menu>

              <v-btn small color="  grey darken-3" text>text</v-btn>
              <v-btn small color="  grey darken-3" text>text</v-btn>
            </div>

            <v-spacer></v-spacer>
            <!-- <v-card elevation="0" width="200">
              <v-text-field
                color="grey darken-3"
                hide-details
                append-icon="mdi-magnify"
                single-line
              ></v-text-field>
            </v-card> -->
            <v-btn large color="grey darken-3" icon
              ><v-icon>mdi-magnify</v-icon></v-btn
            >
            <v-btn large color="grey darken-3" icon
              ><v-icon>mdi-package-variant</v-icon></v-btn
            >

            <v-badge bordered color="orange" overlap dot
              ><v-btn
                @click.stop="rightDrawer = !rightDrawer"
                large
                color="grey darken-3"
                icon
                ><v-icon>mdi-cart</v-icon></v-btn
              ></v-badge
            ></v-col
          ></v-row
        >
      </v-container>
    </v-app-bar>
    <v-navigation-drawer v-model="rightDrawer" right fixed temporary>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <Nuxt />
    </v-main>

    <v-footer elevation="5" padless>
      <v-card flat tile class="text-center">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="pt-0">
          Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet.
          Mauris cursus commodo interdum. Praesent ut risus eget metus luctus
          accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim
          a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula
          lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus
          iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum
          tempor vel ut orci. Orci varius natoque penatibus et magnis dis
          parturient montes, nascetur ridiculus mus.
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text>
          {{ new Date().getFullYear() }} — <strong>Zuna</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      rightDrawer: false,
      drawer: false,
      icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      categories: [
        {
          name: "Утас",
        },
        {
          name: "Консол",
        },
        {
          name: "Дагалдах хэрэгсэл",
        },
      ],

      productphone: [
        {
          name: "iPhone 14",
          link: "/iPhone",
        },
        {
          name: "iPhone 14 Pro",
          link: "/iPhone",
        },
        {
          name: "iPhone 14 Pro Max",
          link: "/iPhone",
        },
        {
          name: "Galaxy Fold 4",
          link: "/iPhone",
        },
        {
          name: "Galaxy Flip 4",
          link: "/iPhone",
        },
        {
          name: "Samsung S23",
          link: "/iPhone",
        },
        {
          name: "Samsung S23 Plus",
          link: "/iPhone",
        },
        {
          name: "Samsung S23 Ultra",
          link: "/iPhone",
        },
      ],
      title: "Vuetify.js",
    };
  },
};
</script>
