<template>
  <v-container fluid pa-0>
    <v-layout wrap justify-center>
      <v-flex
        xs12
        class="main title-container elevation-6 d-flex align-center justify-right"
      >
        <v-flex>
          <span class="sitetitle">כל התחנות</span><br />
          <v-flex xs3 pt-2>
            <v-divider class="divider"></v-divider>
          </v-flex>
        </v-flex>
      </v-flex>
   <v-flex lg10 xs12 mx-auto>
        <v-container>
          <div class="container-svg">
            <img class="svg" src="fill/side-el.svg" />
            <img class="svg" src="fill/side-el1.svg" style="top:100px;" />
            <img class="svg" src="fill/side-el2.svg" style="top:140px;" />
          </div>

          <v-layout wrap align-content-space-around>
            <v-layout row align-content-center wrap>
              <v-flex pa-3 lg4 v-for="card in cards" :key="card.title">
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
          <div class="container-svg" style="bottom:500px">
            <img class="svg" src="fill/side-el.svg" />
            <img class="svg" src="fill/side-el2.svg" style="top:100px;" />
          </div>
        </v-container>
      </v-flex>
    </v-layout>
  </v-container>
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
        { title: 'Psytrance7', src: '/photos/stations/red-sand.jpg' },
      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>
