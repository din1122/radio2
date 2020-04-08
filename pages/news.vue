<template>
  <v-layout wrap justify-center>
    <v-flex
      xs12
      class="main title-container elevation-6 d-flex align-center justify-right"
    >
      <v-flex>
        <span class="sitetitle">חדשות</span><br />
        <v-flex xs2 pt-2>
          <v-divider class="divider"></v-divider>
        </v-flex>
      </v-flex>
    </v-flex>
    <v-flex mx-auto lg9 xs12 pa-3>
      <div class="svgs-index-block" style="top:50vh; left:-14vh;">
        <img class="svg" src="fill/pink-el.svg" style="left: 6vh; top: 10vh;" />
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
      <v-flex pb-3 class="subtitle-box">
        <span class=" stations-text">חם</span>
      </v-flex>
      <!-- mobile -->
      <v-flex d-flex d-sm-none pa-2 v-for="hot in hots" :key="hot.title">
        <v-card class="mx-auto">
          <v-img class="white--text align-end" height="200px" :src="hot.src">
          </v-img>

          <v-card-subtitle class="subtitle">{{ hot.title }}</v-card-subtitle>
          <v-card-actions class="d-block">
            <div class="text-left">
              <v-btn d-inline rounded class="Readmore"> קרא עוד</v-btn>
            </div>
          </v-card-actions>
        </v-card>
      </v-flex>

      <v-flex d-none d-sm-flex>
        <v-layout warp reverse d-none d-sm-flex>
          <v-flex xs8 pa-2>
            <v-card max-width="100%">
              <v-img
                class="white--text align-end"
                height="100%"
                :src="hots[0].src"
              >
                <div
                  class="card-text-box text-right float-left"
                  style="width:90%;"
                >
                  <v-card-title
                    class="d-block"
                    style="height:100% !important;"
                    >{{ hots[0].title }}</v-card-title
                  >
                </div>
              </v-img>
            </v-card>
          </v-flex>
          <v-flex xs4 pa-2>
            <v-layout wrap>
              <v-flex d-flex>
                <v-card max-width="100%">
                  <v-img
                    class="white--text align-end"
                    height="100%"
                    :src="hots[1].src"
                  >
                    <div class="card-text-box text-right">
                      <v-card-title
                        class="d-block"
                        style="height:100% !important;"
                        align-right
                        >{{ hots[1].title }}</v-card-title
                      >
                    </div>
                  </v-img>
                </v-card>
              </v-flex>
              <v-flex d-flex pt-2>
                <v-card max-width="100%">
                  <v-img
                    class="white--text align-end"
                    height="100%"
                    :src="hots[2].src"
                  >
                    <div class="card-text-box text-right">
                      <v-card-title
                        class="d-block"
                        style="height:100% !important;"
                        >{{ hots[2].title }}</v-card-title
                      >
                    </div>
                  </v-img>
                </v-card>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex>
        <v-flex pb-3 class="subtitle-box">
          <span class=" stations-text">פסטיבלים</span>
        </v-flex>
        <v-layout warp row>
          <v-flex
            d-flex
            d-sm-none
            pa-2
            v-for="festival in festivals"
            :key="festival.title"
          >
            <v-card class="mx-auto">
              <v-img
                class="white--text align-end"
                height="200px"
                :src="festival.src"
              >
              </v-img>

              <v-card-subtitle class="subtitle">{{
                festival.title
              }}</v-card-subtitle>
              <v-card-actions class="d-block">
                <div class="text-left">
                  <v-btn d-inline rounded class="Readmore"> קרא עוד</v-btn>
                </div>
              </v-card-actions>
            </v-card>
          </v-flex>
          <v-flex
            d-none
            d-sm-flex
            pa-3
            xs4
            v-for="festival in festivals"
            :key="festival.title"
          >
            <v-card max-width="436">
              <v-img
                class="white--text align-end"
                height="302px"
                :src="festival.src"
              >
                <div class="card-text-box">
                  <v-card-title
                    class="d-block"
                    style="height:100% !important;"
                    align-center
                    >{{ festival.title }}</v-card-title
                  >
                </div>
              </v-img>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex>
        <v-flex pb-3 class="subtitle-box">
          <span class=" stations-text">מוזיקה</span>
        </v-flex>
        <v-layout warp row>
          <v-flex
            d-flex
            d-sm-none
            pa-2
            v-for="music in musics"
            :key="music.title"
          >
            <v-card class="mx-auto">
              <v-img
                class="white--text align-end"
                height="200px"
                :src="music.src"
              >
              </v-img>

              <v-card-subtitle class="subtitle">{{
                music.title
              }}</v-card-subtitle>
              <v-card-actions class="d-block">
                <div class="text-left">
                  <v-btn d-inline rounded class="Readmore"> קרא עוד</v-btn>
                </div>
              </v-card-actions>
            </v-card>
          </v-flex>
          <v-flex
            d-none
            d-sm-flex
            pa-3
            xs4
            v-for="music in musics"
            :key="music.title"
          >
            <v-card max-width="436">
              <v-img
                class="white--text align-end"
                height="302px"
                :src="music.src"
              >
                <div class="card-text-box">
                  <v-card-title
                    class="d-block"
                    style="height:100% !important;"
                    align-center
                    >{{ music.title }}</v-card-title
                  >
                </div>
              </v-img>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex>
        <v-flex pb-3 class="subtitle-box">
          <span class=" stations-text">גלריית פסטיבילים ותמונות</span>
        </v-flex>

        <v-layout warp row>
          <v-flex
            d-flex
            d-sm-none
            pa-2
            v-for="gallery in gallerys"
            :key="gallery.title"
          >
            <v-card class="mx-auto">
              <v-img
                class="white--text align-end"
                height="200px"
                :src="gallery.src"
              >
              </v-img>

              <v-card-subtitle class="subtitle">{{
                gallery.title
              }}</v-card-subtitle>
              <v-card-actions class="d-block">
                <div class="text-left">
                  <v-btn d-inline rounded class="Readmore"> קרא עוד</v-btn>
                </div>
              </v-card-actions>
            </v-card>
          </v-flex>

          <v-flex
            d-none
            d-sm-flex
            pa-3
            xs4
            v-for="gallery in gallerys"
            :key="gallery.title"
          >
            <v-card max-width="436">
              <v-img
                class="white--text align-end"
                height="302px"
                :src="gallery.src"
              >
                <div class="card-text-box">
                  <v-card-title
                    class="d-block"
                    style="height:100% !important;"
                    align-center
                    >{{ gallery.title }}</v-card-title
                  >
                </div>
              </v-img>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
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
      hots: [
        {
          id: 1,
          title: 'Hot1',
          src: require('~/assets/photos/events/festival1.jpg')
        },
        {
          id: 2,
          title: 'Hot2',
          src: require('~/assets/photos/events/festival2.jpg')
        },
        {
          id: 3,
          title: 'Hot3',
          src: require('~/assets/photos/events/festival3.jpg')
        }
      ],
      festivals: [
        {
          title: "פסטיבל מיראג' בסיני פסח2",
          src: require('~/assets/photos/events/festival1.jpg')
        },
        {
          title: "פסטיבל מיראג' בסיני פסח1",
          src: require('~/assets/photos/events/festival2.jpg')
        },
        {
          title: "פסטיבל מיראג' בסיני פסח3",
          src: require('~/assets/photos/events/festival3.jpg')
        }
      ],
      musics: [
        {
          title: "פסטיבל מיראג' בסיני פסח3",
          src: require('~/assets/photos/events/festival4.jpg')
        },
        {
          title: "פסטיבל מיראג' בסיני פסח2",
          src: require('~/assets/photos/events/festival5.jpg')
        },
        {
          title: "פסטיבל מיראג' בסיני פסח1",
          src: require('~/assets/photos/events/festival2.jpg')
        }
      ],
      gallerys: [
        {
          title: "פסטיבל מיראג' בסיני פסח3",
          src: require('~/assets/photos/events/festival5.jpg')
        },
        {
          title: "פסטיבל מיראג' בסיני פסח2",
          src: require('~/assets/photos/events/festival1.jpg')
        },
        {
          title: "פסטיבל מיראג' בסיני פסח1",
          src: require('~/assets/photos/events/festival2.jpg')
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>
