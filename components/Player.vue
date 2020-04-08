<template>
  <v-layout row align-center justify-lg-space-between reverse>
    <audio ref="player">
      <source v-bind:src="playlist[0].src" type="audio/mpeg" v-bind="audio" />
    </audio>
    <v-flex lg1 offset-lg1 xs3 sm2 class="playbtn-box">
      <v-btn class="playbtn" :elevation="0" :ripple="false" @click="!play()">
        <v-icon large class="playicon">{{ icon }}</v-icon>
      </v-btn>
    </v-flex>
    <!--
    <v-flex xs1 class="controls text-center">
      <v-btn class="play" @click="playSound(playlist[0].src)">
        <v-icon>{{ icon }}</v-icon>
      </v-btn>
    </v-flex>
    -->
    <!-- on mobile -->
    <v-flex xs9 d-flex d-sm-none>
      <v-layout wrap>
            <v-flex pl-2 xs12 text-left>
            <span class="song-title">Onkel Dunkel - Beware Of Geeks Bearings Gif's [byt]</span>
          </v-flex>
          <v-flex xs12>
          <v-layout wrap reverse >
      
          <v-flex xs8 >
          <div class="align-center text-right">
            <v-slider
              height="15"
              v-model="media"
              dense
              color="#4BCFAD"
              :prepend-icon="Muted"
              @click:prepend="Mute"
              inverse-label
            >
            </v-slider>
          </div>
        </v-flex>
            <v-flex xs4>
            <div class="svg-like-con">
              <LikeBtn class="like-btn" />
              <LikeBtn class="like-btn upside-like" />
            </div>
          </v-flex>
        </v-layout>
        </v-flex>
      </v-layout>
      </v-flex>

    <v-flex pl-2 xs3 text-left d-none d-sm-flex sm4>
      <span class="">Onkel Dunkel - Beware Of Geeks Bearings Gif's [byt]</span>
    </v-flex>

    <v-flex xs2 d-none d-sm-block sm3>
      <div class="align-center text-right">
        <v-slider
          height="15"
          v-model="media"
          dense
          color="#4BCFAD"
          :prepend-icon="Muted"
          @click:prepend="Mute"
          inverse-label
        >
        </v-slider>
      </div>
    </v-flex>
    <v-flex xs1 class="d-none d-sm-block">
      <div class="svg-like-con">
        <LikeBtn class="like-btn" />
        <LikeBtn class="like-btn upside-like" />
        <!--<img src="icons/like.svg" class="like-btn" />
        <img src="icons/like.svg" class="like-btn upside-like" />
        -->
      </div>
    </v-flex>
    <v-flex xs3 sm2 fill-height pa-0 class="d-none d-sm-block">
      <!--   <img src="photos/stations/green.jpg" alt="Forest"> -->
      <div class="player-card-text-block d-sm-none">
        <v-card-text
          class="display-1 d-flex justify-center align-center fill-height "
        >
          FOREST
        </v-card-text>
      </div>

      <v-img
        height="85px"
        class="align-center card-img"
        :src="require('@/assets/photos/green.jpg')"
      >
      </v-img>
    </v-flex>
  </v-layout>
</template>

<script></script>

<style lang="scss" scoped>
.player-container {
  background: #111;
}
</style>
<script>
import LikeBtn from '~/static/icons/like.svg'
export default {
  components: {
    LikeBtn
  },
  data() {
    return {
      Playerbtn: 'mdi-play',
      audio: '',
      sliderIcon: 'mdi-volume-off',
      media: 0,
      savedVolume: 0,
      volume: '',
      icon: 'mdi-play',
      current: {},
      isPlaying: false,
      controlerVolume: 0,
      index: 0,

      playlist: [
        {
          title: 'sol',
          artist: 'alef',
          src: require('~/assets/songs/Alef.Sol.mp3')
        }
      ]
    }
  },
  mounted() {
    this.controlerVolume = (this.media * 0.01).toPrecision(2)
  },
  computed: {
    Muted() {
      if (this.media == 0) {
        return 'mdi-volume-mute'
      } else {
        return 'mdi-volume-high'
      }
    },
    Mediacontrol() {
      this.media = 50
    }
  },
  methods: {
    Mute() {
      if (this.$refs.player.volume > 0) {
        this.volume = this.$refs.player.volume
        this.savedVolume = this.media
        this.media = 0
        console.log(this.savedVolume)
        this.$refs.player.volume = 0
      } else if (this.$refs.player.volume == 0) {
        if (this.savedVolume == 0) {
          this.media = 10
          this.$refs.player.volume = 0.1
        } else {
          this.$refs.player.volume = this.savedVolume * 0.01
          this.media = this.savedVolume
        }
      }
    },

    play() {
      if (this.isPlaying != true) {
        this.$refs.player.play()
        this.isPlaying = true
        this.icon = 'mdi-pause'
      } else {
        this.$refs.player.pause()
        this.isPlaying = false
        this.icon = 'mdi-play'
      }
    }
  }
}
</script>
<style>
.player-toolbar .v-toolbar__content {
  align-items: unset;
  padding: 0;
}
.v-input__slot {
  display: block !important;
}
.playbtn.v-btn::before {
  background-color: transparent !important;
}
.upside-like {
  transform: rotate(180deg);
}
</style>
