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
      <v-btn
        icon
        @click.stop="drawer = !drawer"
      >
        <v-icon>menu</v-icon>
      </v-btn>
    </v-toolbar>
    <v-navigation-drawer
      temporary
      app
      clipped
      right
      fixed
      v-model="drawer"
    >
      <v-list>
        <v-list-tile 
        @click.native="drawer = !drawer">
          <v-list-tile-action>
            <v-icon light>chevron_right</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>MENU</v-list-tile-title>
        </v-list-tile>
      </v-list>
      <v-list>
        <v-list-tile v-for="page in pages" :key="page.id" :to="page.to">
          <v-list-tile-action>
            <v-icon>{{page.icon}}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
              <v-list-tile-title>
                {{page.title}}
              </v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
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

<script>
  export default {
    data () {
      return {
        drawer: false,
        pages: [
          { id: 1, icon: 'apps', title: 'Portfolio', to: '/portfolio' },
          { id: 2, icon: 'bubble_chart', title: 'Resources', to: '/resources' }
        ],
        rightDrawer: true,
        clipped: true
      }
    }
  }
</script>

<style>
.theme--dark .navigation-drawer {
  background-color: #004356;
}
.navigation-drawer > .list .list__tile--active .list__tile__title {
  color: #e5ecee;
    font-size: large;
}
.list__tile--active .list__tile__action:first-of-type .icon {
  color: #e5ecee;
}
</style>
