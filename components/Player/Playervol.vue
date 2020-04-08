<template>
  <div>
    <audio ref="player" controls>
      <source v-bind:src="playlist[0].src" type="audio/mpeg" v-bind="audio" />
    </audio>

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
</template>

<script>
export default {
  data() {
    return {
      audio: '',
      sliderIcon: 'mdi-volume-off',
      media: 0,
      savedVolume: 0,
      volume: '',
      icon: 'mdi-play',
      current: {},
      isPlaying: false,
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
    this.$vuetify.rtl = false
  },
   mounted() {
    this.$refs.player.volume = (this.media * 0.01).toPrecision(2)
  },
  computed: {
    Muted() {
      if (this.media == 0) {
        return 'mdi-volume-mute'
      } else {
        return 'mdi-volume-off'
      }
    }
  },
  methods: {
    Mute() {
      if (this.$refs.player.volume > 0) {
        this.icon = 'mdi-volume-mute'
        this.volume = this.$refs.player.volume
        this.savedVolume = this.media
        this.media = 0
        console.log(this.savedVolume.toPrecision(1))
        this.$refs.player.volume = 0
      } else if (this.$refs.player.volume == 0) {
        this.$refs.player.volume = this.volume
        this.media = this.savedVolume
      }
    },
    play() {
      if (this.isPlaying != true) {
        this.$refs.player.play()
        this.isPlaying = true
        this.icon = 'mdi-pauese'
      } else {
        this.$refs.player.pause()
        this.isPlaying = false
        this.icon = 'mdi-play'
      }
    }
  }

}
</script>

<style lang="scss" scoped></style>
