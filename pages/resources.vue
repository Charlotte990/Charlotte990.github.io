<template>
  <v-container>
    <div
    class="newPurple text-md-center display-2"
    >
    LANGUAGES
    </div>
      <v-tabs fixed icons centered>
        <v-tabs-bar grow dark class="newPurple">
          <v-tabs-slider color="yellow accent-5"></v-tabs-slider>
          <v-tabs-item 
            v-for="item in items"
            :key="item.id"
            :href="'#tab-' + item.id" >
            <v-icon>{{item.icon}}</v-icon>
            {{item.title}}
          </v-tabs-item>
        </v-tabs-bar>
        <v-tabs-items>
          <v-tabs-content
            v-for="item in items"
            :key="item.id"
            :id="'tab-' + item.id"
          >
          <v-card flat>
          <v-layout class= "newPurpleTwo">
            <v-flex xs6>
              <v-card-text
              >
                {{ item.text }}
              </v-card-text>
            </v-flex>
            <v-flex class="text-md-center">
              <v-card-text>
                <v-icon>
                  {{item.icon}}
                </v-icon>
              </v-card-text>
            </v-flex>
          </v-layout>
          </v-card>
          </v-tabs-content>
        </v-tabs-items>
      </v-tabs>
      </v-container>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {id: 1, title: "Python", text: 'https://www.python.org/', icon: 'fa-bolt'},
          {id: 2, title: "GoLang", text: "https://golang.org/", icon: 'fa-google'}
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