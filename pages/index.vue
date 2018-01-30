<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap>
      <v-flex xs12>
        <v-card color="white elevation-0">
          <v-card-text>
            <img src="/colorlogotransmall.png" alt="Vuetify.js" class="my-4" width="300px" />
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row wrap>
      <v-flex xs4 v-for="section in sections" :key="section.id">
        <v-card color="cyan accent-5">
          <v-card-title style="text-align: center;" class="headline">{{section.name}}</v-card-title>
          <v-card-text>
            <p>Please give me some content. So that I am not boring. Ta very much.</p>
            <img :src='section.img' height="100px"/>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
      sections: [
        {id: 1, name: 'I am Title 1', img: 'http://thecatapi.com/api/images/get?format=src&type=gif'},
        {id: 2, name: 'I am Title 2', img: 'v.png'},
        {id: 3, name: 'I am Title 3', img: 'http://thecatapi.com/api/images/get?format=src&type=gif'}
      ]
  })
}
</script>