<template>
  <v-layout wrap justify-center>
    <v-flex
      xs12
      class="main title-container elevation-6 d-flex align-center justify-right"
    >
      <v-flex>
        <span class="sitetitle">אירועים</span><br />
        <v-flex xs2 pt-2>
          <v-divider class="divider"></v-divider>
        </v-flex>
      </v-flex>
    </v-flex>
    <v-flex xs12 lg10 pa-5>
      <div class="svgs-index-block" style="top:50vh;">
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
      <v-flex d-flex d-sm-none pa-2 v-for="event in events" :key="event.title">
        <v-card class="mx-auto">
          <v-img class="white--text align-end" height="200px" :src="event.src">
          </v-img>

          <v-card-subtitle class="subtitle">{{ event.title }}</v-card-subtitle>

          <v-card-text class="text--primary">
            <div>{{ event.desc }}</div>
          </v-card-text>

          <v-card-actions class="d-block">
            <span>{{ event.subtitle }}</span>
            <div class="text-left">
              <v-btn d-inline rounded class="Readmore"> קרא עוד</v-btn>
            </div>
          </v-card-actions>
        </v-card>
      </v-flex>
      <v-flex d-none d-sm-flex v-for="event in events" :key="event.title">
        <v-layout warp pa-3 class="event-card">
          <v-flex xs4>
            <nuxt-link to="/post">
              <v-img :src="event.src" width="100%"></v-img>
            </nuxt-link>
          </v-flex>
          <v-flex xs8 pr-3>
            <v-layout wrap fill-height>
              <v-flex xs12>
                <nuxt-link to="#">
                  <span class="event-title">{{ event.title }}</span></nuxt-link
                ><br />
                <span class="text-right event-subtitle"
                  >{{ event.subtitle }}<v-icon>mdi-dots-horizontal</v-icon
                  ><span>תגובה אחת</span>
                </span>
              </v-flex>
              <v-flex xs12>
                <v-flex xs8>
                  <span class="event-desc">{{ event.desc }}</span>
                </v-flex>
              </v-flex>
              <v-flex mt-auto>
                <v-btn rounded class="Readmore"> קרא עוד</v-btn>
              </v-flex>
            </v-layout>
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
      events: [
        {
          title: "פסטיבל מיראג' בסיני פסח - 10-13.04.2020",
          subtitle: 'Forest, 06 | 01 | 2020',
          desc:
            'פסטיבל מיראג’ בסיני פסח – 10-13.04.2020 היו היה יום בהיר אחד התיישבנו ביחד כל החברים מהיפי טיפי, פאזל אפקט, חסמבה',
          commnets: '',
          src: '/photos/events/festival1.jpg'
        },

        {
          title: "פסטיבל מיראג' בסיני פסח - 10-13.04.2020",
          subtitle: 'Forest, 06 | 01 | 2020',
          desc:
            'פסטיבל מיראג’ בסיני פסח – 10-13.04.2020 היו היה יום בהיר אחד התיישבנו ביחד כל החברים מהיפי טיפי, פאזל אפקט, חסמבה',
          commnets: '',
          src: '/photos/events/festival2.jpg'
        },

        {
          title: "פסטיבל מיראג' בסיני פסח - 10-13.04.2020",
          subtitle: 'Forest, 06 | 01 | 2020',
          desc:
            'פסטיבל מיראג’ בסיני פסח – 10-13.04.2020 היו היה יום בהיר אחד התיישבנו ביחד כל החברים מהיפי טיפי, פאזל אפקט, חסמבה',
          commnets: '',
          src: '/photos/events/festival3.jpg'
        },

        {
          title: "פסטיבל מיראג' בסיני פסח - 10-13.04.2020",
          subtitle: 'Forest, 06 | 01 | 2020',
          desc:
            'פסטיבל מיראג’ בסיני פסח – 10-13.04.2020 היו היה יום בהיר אחד התיישבנו ביחד כל החברים מהיפי טיפי, פאזל אפקט, חסמבה',
          commnets: '',
          src: '/photos/events/festival4.jpg'
        },

        {
          title: "פסטיבל מיראג' בסיני פסח - 10-13.04.2020",
          subtitle: 'Forest, 06 | 01 | 2020',
          desc:
            'פסטיבל מיראג’ בסיני פסח – 10-13.04.2020 היו היה יום בהיר אחד התיישבנו ביחד כל החברים מהיפי טיפי, פאזל אפקט, חסמבה',
          commnets: '',
          src: '/photos/events/festival5.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.v-icon {
  color: #657278;
}
</style>
