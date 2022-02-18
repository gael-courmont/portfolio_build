<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="green--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{project.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-card-title class="cardTitle">
            {{project.title}}
          </v-card-title>
          <v-card-text>
            <h3>Description</h3>
          </v-card-text>
          <v-card-text>
            <p> Ceci est la description du projet sur plusieurs ligne,oui oui vous lisez bien</p>
          </v-card-text>
          <v-card-media>
            <v-img contain max-height="500px" :src="project.poster"></v-img>
          </v-card-media>
          <v-card-text>
            <h3>Demo</h3>

            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="green" text-color="white">{{project.tech.tech1}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech2}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech3}}</v-chip>
            <v-chip color="green" text-color="white">{{project.tech.tech4}}</v-chip>
          </v-card-text>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: 'Diverse Portfolio',
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          'Gael courmont diverse portefolio'
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Eldin' Space" },
      { property: 'og:site_name', content: "Eldin' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://eldin.space' },
      {
        property: 'og:description',
        content:
          'Gael courmont diverse portfolio'
      }
    ]
  },
  data () {
    return {
      dialog: false,
      projects: [
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
    }
  }
}
</script>

<style  scoped>
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
