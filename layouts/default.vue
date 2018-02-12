<template>
  <v-app dark>
    <v-toolbar
    fixed 
    app 
    color="cyan accent-5"
    >
      <v-spacer></v-spacer>
      <v-btn
      icon
      href='http://www.instagram.com'
      target='_blank'
      >
        <v-icon medium>fa-instagram</v-icon>
      </v-btn>
      <v-toolbar-title class="white--text ml-0">
        <v-btn flat color="white" href="/" target='_self'>HOME</v-btn>
      </v-toolbar-title>
      <v-btn 
      icon
      href='http://github.com'
      target='_blank'
      >
        <v-icon medium>fa-github</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-content>
      <v-container ma-2 fluid>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer 
    fixed
    app
    color="cyan accent-5"
    >
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

