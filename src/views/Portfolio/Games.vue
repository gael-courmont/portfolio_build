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
          <v-card-title class="cardTitle">
            {{game.title}}
          </v-card-title>
          <v-card-text>
            <h3>Description</h3>
          </v-card-text>
          <v-card-text>
            <span>{{game.link}}</span>
          </v-card-text>
          <v-card-text>
              <p>{{game.description}}</p>
          </v-card-text>
          <v-card-text>
            <h3>Demo</h3>
          </v-card-text>
          <plyr class="vid">
            <div class="plyr__video-embed">
              <iframe :src="game.href" allowfullscreen allowtransparency allow="autoplay"></iframe>
            </div>
          </plyr>
          <v-card-text>
              <h3 class="headline mb-0">
                <span>Technology</span>
                <span class="right" >Role</span>
              </h3>
              <v-chip color="green" text-color="white">{{game.tech.tech1}}</v-chip>
              <v-chip color="green" text-color="white">{{game.tech.tech2}}</v-chip>
              <v-chip class="right" color="green" text-color="white">{{game.role}}</v-chip>
          </v-card-text>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
import { PlyrVideo } from 'vue-plyr'

export default {
  metaInfo: {
    title: 'Graphic Portfolio ',
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          "Eldin Zaimovic's Graphic Adobe PhotoShop Logo Design Instagram Poster"
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Eldin' Space" },
      { property: 'og:site_name', content: "Eldin' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://eldin.space' },
      {
        property: 'og:game',
        content: 'https://i.imgur.com/Dcz2PGx.jpg'
      },
      {
        property: 'og:description',
        content:
          "Eldin Zaimovic's Graphic Adobe PhotoShop Logo Design Instagram Poster"
      }
    ]
  },
  components: { plyr: PlyrVideo },
  data () {
    return {
      dialog: false,
      project: [
        {
          dialog: false,
          title: 'The Fireflies Express',
          poster: 'https://ggj.s3.amazonaws.com/styles/game_sidebar__wide/featured_image/2022/01/427346/affice_2.png?itok=Ex1vLdDL&timestamp=1643547624',
          href: 'https://youtube.com/embed/KYu0GYQfNEE',
          description: 'Face the dangers of an eerie train with the help of an angel and a demon, and try to reach the exit ! Game made during the Global Game Jam 2022 by a team of 6.',
          link: 'https://globalgamejam.org/2022/games/fireflies-express-1',
          role: 'Unity Developper',
          tech: {
            tech1: 'UNITY',
            tech2: 'PHOTOSHOP'
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
