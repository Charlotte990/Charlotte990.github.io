<template>
  <v-container grid-list-md text-xs-center>
    <v-layout>
      <v-flex text-xs-center>
        <img src="/colorlogotransmall.png" alt="Vuetify.js" class="mb-5">
        <h2 class="primary">PORTFOLIO</h2>
          <v-layout row wrap>
            <v-flex xs6 v-for="item in items" :key="item.id">
              <v-card>
                <v-card-media v-bind:src="item.src" height="400px">
                </v-card-media>
                <v-card-title primary-title>
                    <v-btn flat color="white" :href="item.url" target='_blank'>{{item.siteName}}</v-btn>
                    <v-spacer></v-spacer>
                    <div>{{item.description}}</div>
                </v-card-title>
              </v-card>
            </v-flex>
          </v-layout>
        <footer>
        </footer>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            id: 1, src: '/untappedzoomout.png', siteName: "Untapped Talent", description: "Business website for a local music studio", url: "http://untappedtalent.co.uk"
          },
          {
            id: 2, src: '/mikebrown.png', siteName: "Mike Brown Illustration", description: "Portfolio, personal website for local illustrator", url: "http://mike-brown.co.uk"
          }
        ]
      }
    }
  }
</script>
