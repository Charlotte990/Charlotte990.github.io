<template>
  <v-container>
    <v-layout xs12>
      <v-flex xs12 align-center text-md-center>
        <img src="/colorlogotransmall.png" alt="Vuetify.js" class="mb-5">
        <h2 class="newPurple">LANGUAGES & RESOURCES</h2>
      </v-flex>
    </v-layout>  
    <v-layout xs12 row wrap>
      <v-flex>
        <v-tabs icons-and-text centered dark color="warning">
          <v-tabs-slider color="yellow"></v-tabs-slider>
          <v-tab 
            v-for="item in items" 
            :key="item.id"
            :href="'#tab-' + item.id"
            >
            {{item.title}}
            <v-icon>{{item.icon}}</v-icon>
          </v-tab>
          <v-tab-item
            v-for="item in items"
            :key="item.id"
            :id="'tab-' + item.id"
          >
            <v-layout xs12 row wrap>
              <v-flex xs6>
                <v-card
                class="text-xs-center"
                tile
                flat
                color="info"
                >
                  <v-card-text>
                    <a class="white--text" :href="item.to" target="_blank">
                      {{ item.to }}
                    </a>
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex>
                <v-card
                class="text-xs-center"
                tile
                flat
                color="info">
                <v-card-text>{{item.other}}</v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-tab-item>
        </v-tabs>
      </v-flex>
    </v-layout>
  </v-container>    
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {id: 1, title: "Python", to: 'https://www.python.org/', other: "CodeWars, Codecademy", icon: 'fa-bolt'},
          {id: 2, title: "GoLang", to: "https://golang.org/", other: "CodeSchool, GoLang Playground", icon: 'fa-google'},
          {id: 3, title: "VueJS", to: "https://vuejs.org/", other: "Vue", icon: 'fa-chevron-down'}
        ]
      }
    }
  }
</script>

<style>

.newYellow {
  background-color: #435600;
}
.newPurple {
  background-color: #560043;
}
.newPurpleTwo {
  background-color: #884c7b;
}
</style>