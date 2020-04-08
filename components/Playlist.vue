<template>
  <div>
    <v-flex xs12 lg8 mx-auto>
      <v-layout
        d-none
        d-sm-flex
        wrap
        mb-5
        v-for="item in items.playlists"
        :key="item.id"
      >
        <v-flex xs8 class="playlist-container">
          <v-flex float-left pa-3 class="playlist-box">
            <v-list>
              <v-list-item reverse v-for="song in item.songs" :key="song.id">
                <v-list-item-content class="text-left">
                  <span>
                    {{ song.title }}
                  </span>
                  <span class="artist-text">
                    {{ song.artist }}
                  </span>
                  <v-divider></v-divider>
                </v-list-item-content>
                <v-list-item-action>
                  <v-btn icon>
                    <v-icon>mdi-minus-circle-outline</v-icon>
                  </v-btn>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-flex>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-img :src="item.src" class="white--text align-end" height="302px">
              <div class="btn-centered">
                <v-btn
                  d-inline
                  class="playbtn playlistbtn"
                  :elevation="0"
                  :ripple="false"
                >
                  <v-icon large class="playicon">{{ icon }}</v-icon>
                </v-btn>
              </div>
              <div class="card-text-box">
                <v-card-title
                  class="d-block"
                  style="height:100% !important;"
                  align-center
                  >{{ item.title }}</v-card-title
                >
              </div>
            </v-img>
          </v-card>
        </v-flex>
      </v-layout>
      <v-layout
        pa-2
        d-flex
        d-sm-none
        v-for="item in items.playlists"
        :key="item.title"
      >
        <v-card class="mx-auto mobile-card">
          <v-img
            class="white--text align-end"
            height="200px"
            src="/photos/stations/green.jpg"
          >
            <v-card-title>Top 10 Australian beaches</v-card-title>
          </v-img>

          <v-card-subtitle class="pb-0">{{ item.title }}</v-card-subtitle>

          <v-card-text class="text--primary">
            <v-list>
              <v-list-item reverse v-for="song in item.songs" :key="song.id">
                <v-list-item-content class="text-left">
                  <span>
                    {{ song.title }}
                  </span>
                  <span class="artist-text">
                    {{ song.artist }}
                  </span>
                  <v-divider></v-divider>
                </v-list-item-content>
                <v-list-item-action>
                  <v-btn icon>
                    <v-icon>mdi-minus-circle-outline</v-icon>
                  </v-btn>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card-text>
        </v-card>
      </v-layout>
    </v-flex>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icon: 'mdi-play',
      items: {
        playlists: [
          {
            id: '1',
            title: 'playlist1',
            src: '/photos/stations/green.jpg',
            songs: [
              { title: 'song1', artist: 'artist', order: 1 },
              { title: 'song1', artist: 'someone3', order: 1 },
              { title: 'song1', artist: 'someone3', order: 1 }
            ]
          },
          {
            id: '2',
            src: '/photos/stations/blue.jpg',
            title: 'playlist2',
            songs: [{ title: 'song2', artist: 'someone3', order: 1 }]
          },
          {
            id: '3',
            src: '/photos/stations/abstract.jpg',
            title: 'playlist3',
            songs: [{ title: 'song3', artist: 'someone3', order: 1 }]
          }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.v-icon {
  color: #4bcfad;
}
.v-list {
  background: transparent;
}
.playlist-box {
  max-height: 300px;
  overflow: auto;
  width: 100%;
  direction: ltr;
}
.btn-centered {
  position: absolute;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.theme--dark.v-btn:not(.v-btn--flat):not(.v-btn--text):not(.v-btn--outlined) {
  background: transparent;
}
.playlistbtn.playbtn.v-btn:not(.v-btn--round).v-size--default {
  width: 100px;
  height: 100px;
}
.mobile-card {
  background: #073770;
}
.v-list-item__content:hover {
  background: #ffffff1f;
  padding: 7px 6px;
  cursor: pointer;
}
</style>
