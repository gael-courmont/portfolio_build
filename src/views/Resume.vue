<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Education</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEPT 2016 -</div>
                <div class="caption font-weight-bold green--text">JAN 2022</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Ingeneer degree specialised in artificial intelligence</strong>
                <div class="caption mb-2">ISEN LILLE</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEP 2016 -</div>
                <div class="caption font-weight-bold green--text">JUNE 2020</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Bachelor of technologie</strong>
                <div class="caption mb-2">ISEN LILLE</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEP 2016 -</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Scientifique Baccalauréat with sport option</strong>
                <div class="caption mb-2">Robespierre highscool Arras</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JULY 2022 -</div>
                <div class="caption font-weight-bold green--text">JANUARY 2023</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Game developer intern</strong>
                <div class="caption mb-2">DTT</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JUNE 2021 -</div>
                <div class="caption font-weight-bold green--text">SEPTEMBER 2021</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>DATA Scientist for deployment purpose</strong>
                <div class="caption mb-2">Diskyver</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JUNE 2019 -</div>
                <div class="caption font-weight-bold green--text">SEPTEMBER 2019</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>General assistant</strong>
                <div class="caption mb-2">prince’s house hotel (Scotland)</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Software</span>

          <span class="green--text">Skills</span>
        </h2>
        <br>
        <strong>Unity</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong> Jenkins</strong>
        <v-progress-linear v-model="buffer2" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>MongoDB/Elasticsearch</strong>
        <v-progress-linear v-model="buffer3" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Coding</span>
          <span class="green--text">Skills</span>
        </h2>
        <br>
        <strong>C++/C#/JAVA</strong>
        <v-progress-linear v-model="buffer4" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>Python</strong>
        <v-progress-linear v-model="buffer5" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>HTML/css/js</strong>
        <v-progress-linear v-model="buffer6" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <div class="mt-4 pt-2">
        <v-btn
          href="https://drive.google.com/file/d/1jX5i3kF8ht3HjBnvNILq-u5iiucuKK0U/view?usp=share_link"
          target="_blank"
          color="green"
          dark
          large
        >
          Download Resume
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Resume',
    titleTemplate: "%s ← Gael's Space",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          'Unity Python Java C# Pytorch keras Vue'
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Gael' Space" },
      { property: 'og:site_name', content: "Gael' Space" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://courmont-gael-portfolio.herokuapp.com' },
      {
        property: 'og:description',
        content:
          'Unity Python Java C# Pytorch keras Vue'
      }
    ]
  },
  data () {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    }
  },
  mounted () {
    this.startBuffer()
  },

  beforeDestroy () {
    clearInterval(this.interval)
  },

  methods: {
    startBuffer () {
      this.interval = setInterval(() => {
        this.buffer1 = 90
        this.buffer2 = 75
        this.buffer3 = 90
        this.buffer4 = 90
        this.buffer5 = 80
        this.buffer6 = 80
      }, 800)
    }
  }
}
</script>
<style >
</style>
