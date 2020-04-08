<template>
  <v-container fluid pa-0>
    <v-layout wrap justify-center>
      <v-flex
        xs12
        class="main title-container elevation-6 d-flex align-center justify-right"
      >
        <v-flex>
          <span class="sitetitle">פלייליסטים</span><br />
          <v-flex xs3 pt-2>
            <v-divider class="divider"></v-divider>
          </v-flex>
        </v-flex>
      </v-flex>
      <v-container>
        <div class="svgs-index-block" style="top:50vh;">
          <img
            class="svg"
            src="fill/pink-el.svg"
            style="left: 6vh; top: 10vh;"
          />
          <img
            class="svg"
            src="fill/cyan-l.svg"
            style="left: 8vh; top: 20vh; z-index: 1;"
          />
          <img
            class="svg"
            src="fill/cyan-l.svg"
            style="left: 8vh; top: 15vh; z-index: 1;"
          />
          <img class="svg cyan-el-index" src="fill/cyan-el.svg" />
        </div>

        <div class="container-svg">
          <img class="svg" src="fill/side-el.svg" />
          <img class="svg" src="fill/side-el1.svg" style="top:100px;" />
          <img class="svg" src="fill/side-el2.svg" style="top:140px;" />
        </div>

        <Playlist />
        <div class="container-svg" style="bottom:500px">
          <img class="svg" src="fill/side-el.svg" />
          <img class="svg" src="fill/side-el2.svg" style="top:100px;" />
        </div>
      </v-container>
    </v-layout>
  </v-container>
</template>

<script>
import Playlist from '~/components/Playlist.vue'
export default {
  data() {
    return {}
  },
  components: {
    Playlist
  }
}
</script>

<style lang="scss" scoped></style>
