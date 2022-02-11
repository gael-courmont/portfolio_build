<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Video</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="video.dialog"
        lazy
        max-width="800"
        v-for="video in videos"
        :key="video.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="video.poster"
                aspect-ratio="1.7778"
                :alt="video.title"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
                contain
              ></v-img>
              <v-card-title primary-title class="justify-center">{{video.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="video.dialog">
          <v-card-title class="cardTitle">
            {{video.title}}
          </v-card-title>
          <v-card-text>
            <h3>Description</h3>
          </v-card-text>
          <v-card-text>
            <p> Ceci est la description du projet sur plusieurs ligne,oui oui vous lisez bien</p>
          </v-card-text>
          <v-card-text>
            <h3>Demo</h3>
          </v-card-text>
          <plyr class="vid">
            <div class="plyr__video-embed">
              <iframe :src="video.href" allowfullscreen allowtransparency allow="autoplay"></iframe>
            </div>
          </plyr>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="green" text-color="white">{{video.tech.tech1}}</v-chip>
            <v-chip color="green" text-color="white">{{video.tech.tech2}}</v-chip>
            <v-chip color="green" text-color="white">{{video.tech.tech3}}</v-chip>
            <v-chip color="green" text-color="white">{{video.tech.tech4}}</v-chip>
          </v-card-text>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
import { PlyrVideo } from "vue-plyr";

export default {
  metaInfo: {
    title: "Video Portfolio",
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Eldin Zaimovic's Services Adobe Premire After Effects Video Ad's Social Media Logo Animation Instagram Facebook Video Editing Advetising"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Eldin' Space" },
      { property: "og:site_name", content: "Eldin' Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://eldin.space" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      {
        property: "og:description",
        content:
          "Eldin Zaimovic's Services Adobe Premire After Effects Video Ad's Social Media Logo Animation Instagram Facebook Video Editing Advetising"
      }
    ]
  },
  components: { plyr: PlyrVideo },
  data() {
    return {
      dialog: false,
      videos: [
        {
          dialog: false,
          title: 'VilaShirts Logo',
          poster: 'https://i.imgur.com/QEnmqcE.png',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'BlackBird Property Group Logo',
          poster: 'https://i.imgur.com/b37FfUU.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'TeeLock Consulting Logo',
          poster: 'https://i.imgur.com/XSo4bmw.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'SEA||WA||MMXI',
          poster: 'https://i.imgur.com/thxUnTH.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'Alpine365 Logo',
          poster: 'https://i.imgur.com/LOzW21e.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'Josefine Product Pack',
          poster: 'https://i.imgur.com/TrthgRN.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'Next Party Flayer',
          poster: 'https://i.imgur.com/tYjfL2d.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'VilaShirts T-Shirts',
          poster: 'https://i.imgur.com/ULuRuFB.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        },
        {
          dialog: false,
          title: 'BAB Coin',
          poster: 'https://i.imgur.com/YU52AVB.jpg',
          href: 'https://www.youtube.com/embed/XP8j7NA_wzc',
          tech: {
            tech1: 'VUE',
            tech2: 'GraphQL',
            tech3: 'Axios',
            tech4: 'JavaScript'
          }
        }
      ]
    };
  }
};
</script>

<style  scoped>
@import "../../../node_modules/vue-plyr/dist/vue-plyr.css";
.cardTitle{
  text-align: center;
  color: green ;
  font-size: x-large;
  justify-content: center;
}
.vid{
  text-align: center;
}
</style>
