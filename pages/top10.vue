<template>
  <v-layout wrap justify-center>
    <v-flex
      xs12
      class="main title-container elevation-6 d-flex align-center justify-right"
    >
      <v-flex>
        <span class="sitetitle">עשר תחנות מובילות</span><br />
        <v-flex xs3 pt-2>
          <v-divider class="divider"></v-divider>
        </v-flex>
      </v-flex>
    </v-flex>
    <v-flex lg8 xs12 >
      <div class="container-svg">
        <img class="svg" src="fill/side-el.svg" />
        <img class="svg" src="fill/side-el1.svg" style="top:100px;" />
        <img class="svg" src="fill/side-el2.svg" style="top:140px;" />
      </div>
      <v-layout wrap>
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
        <!--
   <v-flex v-for="station in stations" :key="station.title" pa-3  d-flex d-sm-none >
       <v-card >
                <v-img
                  class="white--text align-end"
                  height="105px"
                  :src="station.src"
                >
                  <div class="card-text-box">
                    <v-card-title
                      class="d-block"
                      style="height:100% !important;"
                      align-center
                      >{{ station.title}}</v-card-title
                    >
                  </div>
                </v-img>
              </v-card>
     </v-flex>
     -->
     
        <v-flex v-for="station in stations" :key="station.title" pa-3>

          <v-card >
            <v-img
              height="200px"
              class="card-img"
              :src="station.src"
            >
              <div class="card-text-block">
                <v-card-title
                  class="display-2 d-block d-xs-flex justify-center align-center fill-height"
                >
                  {{ station.title }}
                </v-card-title>
              </div>
            </v-img>
          </v-card>
        </v-flex>
      </v-layout>
      <div class="container-svg" style="bottom:500px">
        <img class="svg" src="fill/side-el.svg" />
        <img class="svg" src="fill/side-el2.svg" style="top:100px;" />
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      stations: [
         { title: 'FOREST', src: '/photos/stations/green.jpg' },
        { title: 'DarkPsy', src: '/photos/stations/abstract.jpg' },
        { title: 'PSYCHODELIC', src: '/photos/stations/blue.jpg' },
        { title: 'Chillstep', src: '/photos/stations/green-red.jpg' },
        { title: 'Zenon', src: '/photos/stations/pink-purple.jpg' },
        { title: 'Psytrance-first', src: '/photos/stations/pink-yellow.jpg' },
        { title: 'Psytrance', src: '/photos/stations/red-sand.jpg' },
      ]
    }
  }
}
</script>
 
<style lang="scss" scoped>
</style>
