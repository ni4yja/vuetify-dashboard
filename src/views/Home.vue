<template>
  <v-app id="inspire">
    <SideBar />
    <v-container>
      <v-app-bar color="rgba(0,0,0,0)" flat>
        <v-text-field
          label="Search..."
          class="pt-5"
          filled
          prepend-inner-icon="mdi-magnify"
          dense
          solo
          flat
          background-color="grey lighten-4"
          rounded
        >
        </v-text-field>
        <v-spacer></v-spacer>
        <v-btn icon dark>
          <v-icon color="black">far fa-bell</v-icon>
        </v-btn>
        <v-select
          class="mt-7"
          :items="items"
          v-model="select"
          item-text="state"
          color="black"
          solo
          flat
          style="max-width: 7%"
          item-color="grey darken-2"
        ></v-select>
        <span text color="#878194">AAE IdeaPro</span>
        <v-avatar size="30" class="ml-2">
          <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"></v-img>
        </v-avatar>
      </v-app-bar>
    </v-container>
  </v-app>
</template>

<script>
import SideBar from "../components/SideBar";

export default {
  name: "Home",
  components: {
    SideBar,
  },
  data: () => ({
    select: { state: "EN" },
    items: ["EN", "ES", "UA"],
    text: "weekly",
    width: 2,
    radius: 10,
    padding: 8,
    lineCap: "round",
    value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0],
    fill: false,
    type: "trend",
    autoLineWidth: false,
    slides: [
      { src: require("../../public/01.jpg") },
      { src: require("../../public/02.jpg") },
      { src: require("../../public/03.jpg") },
      { src: require("../../public/04.jpg") },
      { src: require("../../public/05.jpg") },
      { src: require("../../public/06.jpg") },
      { src: require("../../public/07.png") },
      { src: require("../../public/08.png") },
      { src: require("../../public/09.jpg") },
      { src: require("../../public/10.jpg") },
      { src: require("../../public/11.jpg") },
      { src: require("../../public/12.jpg") },
    ],
  }),
};
</script>
