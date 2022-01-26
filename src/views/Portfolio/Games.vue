<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Graphic</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="game.dialog"
        lazy
        max-width="800"
        v-for="game in project"
        :key="game.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="game.poster"
                height="230"
                :alt="game.title"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{game.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="game.dialog">
          <v-img :src="game.poster"></v-img>
          <iframe :src="game.href" allowfullscreen allowtransparency allow="autoplay"></iframe>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
import { PlyrVideo } from "vue-plyr";

export default {
  metaInfo: {
    title: "Graphic Portfolio ",
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Eldin Zaimovic's Graphic Adobe PhotoShop Logo Design Instagram Poster"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Eldin' Space" },
      { property: "og:site_name", content: "Eldin' Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://eldin.space" },
      {
        property: "og:game",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      {
        property: "og:description",
        content:
          "Eldin Zaimovic's Graphic Adobe PhotoShop Logo Design Instagram Poster"
      }
    ]
  },
  components: { plyr: PlyrVideo },
  data() {
    return {
      dialog: false,
      project: [
        {
          dialog: false,
          title: "VilaShirts Logo",
          poster: "https://i.imgur.com/QEnmqcE.png",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc",
        },
        {
          dialog: false,
          title: "BlackBird Property Group Logo",
          poster: "https://i.imgur.com/b37FfUU.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc",
        },
        {
          dialog: false,
          title: "TeeLock Consulting Logo",
          poster: "https://i.imgur.com/XSo4bmw.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc",
        },
        {
          dialog: false,
          title: "SEA||WA||MMXI",
          poster: "https://i.imgur.com/thxUnTH.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc",
        },
        {
          dialog: false,
          title: "Alpine365 Logo",
          poster: "https://i.imgur.com/LOzW21e.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc",
        },
        {
          dialog: false,
          title: "Josefine Product Pack",
          poster: "https://i.imgur.com/TrthgRN.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc",
        },
        {
          dialog: false,
          title: "Next Party Flayer",
          poster: "https://i.imgur.com/tYjfL2d.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc"
        },
        {
          dialog: false,
          title: "VilaShirts T-Shirts",
          poster: "https://i.imgur.com/ULuRuFB.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc"
        },
        {
          dialog: false,
          title: "BAB Coin",
          poster: "https://i.imgur.com/YU52AVB.jpg",
          href: "https://www.youtube.com/embed/XP8j7NA_wzc"
        }
      ]
    };
  }
};
</script>

<style  scoped>
</style>