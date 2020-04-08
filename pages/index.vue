<template>
  <v-layout wrap>
    <v-flex xs12 class="main welcome-container elevation-6">
      <v-flex pa-3 lg8>
        <span class="sitetitle">תחנות מוזיקה פסיכודלית</span><br />
        <span class="subtitle">אצלנו תקבל מסאז' למוח</span>
        <v-flex class="divider-container">
          <v-divider class="divider"></v-divider>
        </v-flex>
        <div class="svgs-index-block">
          <img
            class="svg pink-cir"
            src="fill/pink-el.svg"
          />
          <img
            class="svg cyan-line1"
            src="fill/cyan-l.svg"

          />
          <img
            class="svg cyan-line"
            src="fill/cyan-l.svg"
          />
          <img class="svg cyan-el-index" src="fill/cyan-el.svg" />
        </div>
      </v-flex>
      <br />
      <v-flex>
        <v-spacer></v-spacer>
        <v-btn rounded text class="signup-btn" large>הירשם עכשיו</v-btn>
      </v-flex>
    </v-flex>
    <v-flex lg10 xs12 mx-auto>
      <v-container>
        <div class="container-svg d-sm-block">
          <img class="svg" src="fill/side-el.svg" />
          <img class="svg" src="fill/side-el1.svg" style="top:100px;" />
          <img class="svg" src="fill/side-el2.svg" style="top:140px;" />
        </div>
        <v-layout wrap align-content-space-around>
          <v-flex pb-3 class="subtitle-box">
            <span class=" stations-text">תחנות</span>
          </v-flex>
          <v-layout row align-content-center wrap>
            <v-flex pa-3 lg4 sm6 v-for="card in cards" :key="card.title">
              <v-card max-width="436">
                <v-img
                  class="white--text align-end"
                  height="302px"
                  :src="card.src"
                >
                  <div class="card-text-box">
                    <v-card-title
                      class="d-block"
                      style="height:100% !important;"
                      align-center
                      >{{ card.title }}</v-card-title
                    >
                  </div>
                </v-img>
              </v-card>
            </v-flex>
          </v-layout>
        </v-layout>
        <div class="container-svg d-sm-block" style="bottom:500px">
          <img class="svg" src="fill/side-el.svg" />
          <img class="svg" src="fill/side-el2.svg" style="top:100px;" />
        </div>
      </v-container>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        { title: 'Psytrance1', src: '/photos/stations/green.jpg' },
        { title: 'Psytrance2', src: '/photos/stations/abstract.jpg' },
        { title: 'Psytrance3', src: '/photos/stations/blue.jpg' },
        { title: 'Psytrance4', src: '/photos/stations/green-red.jpg' },
        { title: 'Psytrance5', src: '/photos/stations/pink-purple.jpg' },
        { title: 'Psytrance6', src: '/photos/stations/pink-yellow.jpg' },
        { title: 'Psytrance7', src: '/photos/stations/red-sand.jpg' }
      ]
    }
  }
}
</script>
<style></style>
