<template>
  <v-app>
    <v-app-bar fixed app right>
      <v-list-item-icon>
        <v-icon>mdi-magnify</v-icon>
      </v-list-item-icon>
      
      <v-list-item-icon class="d-lg-none">
        <v-icon   @click.stop="drawer = !drawer" >mdi-menu</v-icon>
      </v-list-item-icon>
         <v-spacer></v-spacer>
      <div class="d-none d-sm-block">
          <v-btn small :to="{ path: 'login' }">
            <span>התחבר</span>
          </v-btn>
          <v-btn small class="register-btn" :to="{ path: 'register' }">
            <span>הירשם</span>
          </v-btn>
      </div>

       <div class="d-block d-lg-none">
         <v-list-item
          :ripple="false"
          active-class
          link
          :to="{ path: '/' }"
          class="home-btn display-1 "
        >
          {{ title }}
        </v-list-item>
        </div>
    </v-app-bar>
    <v-content>
      <v-navigation-drawer
        class="main-nav"
        v-model="drawer"
        :mini-variant="mini"
        mini-variant-width="120"
        right
        app
      >
        <v-list-item
          :ripple="false"
          active-class
          link
          :to="{ path: '/' }"
          class="home-btn display-1"
        >
          {{ title }}
        </v-list-item>
        <v-list-item class=" menu-icon" link @click.stop="mini = !mini">
          <v-icon>mdi-menu</v-icon>
        </v-list-item>
        <v-list dense>
          <v-list-item
            router
            exact
            v-for="(item, i) in items"
            :key="i"
            :to="item.link"
            link
            class="item-list"
          >
            <v-list-item-icon class="text-center menu-icon">
              <img :src="`icons/${item.icon}`" />
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title class="subtitle-1 ">{{
                item.title
              }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <v-app-bar
        height="85"
        class="player-toolbar"
        pa-0
        app
        bottom
        clipped-right
      >
        <Player />
      </v-app-bar>
      <v-container fluid pa-0 class="app">
        
        <nuxt />
      </v-container>
      <sitefooter />
    </v-content>
  </v-app>
</template>

<script>

import Top10 from '~/static/icons/top10.svg'
import sitefooter from '~/components/Footer.vue'
import Player from '~/components/Player.vue'
export default {
  data() {
    return {
      drawer: true,
      items: [
        { title: '10 תחנות מובילות', icon: 'top10.svg', link: 'top10' },
        { title: 'כל התחנות', icon: 'radio.svg', link: 'radio' },
        { title: 'פלייליסטים', icon: 'playlists.svg', link: 'playlists' },
        { title: 'אירועים', icon: 'events.svg', link: 'events' },
        { title: 'חדשות', icon: 'news.svg', link: 'news' },
        { title: 'תרומות', icon: 'donate.svg', link: 'donate' }
      ],
      mini: true,
      title: 'LOGO'
    }
  },
  components: {
    sitefooter,
    Player,
    // svgs
    Top10,
  }
}
</script>
<style>
.v-list-item {
}
.menu {
  padding: 0 16px !important;
}
.main-nav {
  border-left: 4px solid #4bcfad;
}
.register-btn {
  background: #4bcfad !important;
  color: black !important;
  font-weight: 200;
  margin-right: 20px !important;
}
.menu-text {
  font-size: 16px;
}
.item-list {
  margin-bottom: 15px;
}
.menu-icon {
  margin-bottom: 15px;
}
</style>
