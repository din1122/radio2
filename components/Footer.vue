<template>
  <v-footer dark padless>
    <v-layout wrap>
      <v-flex text-center lg3 sm6 xs12>
        <div class="pa-3">
          <span class="footer-title">תפריט</span>
        </div>
        <li v-for="li in menu" :key="li.title" class="footer-list">
          <v-btn :ripple="false" depressed to href>{{ li.title }}</v-btn>
        </li>
      </v-flex>
      <v-flex text-center  lg3 sm6 xs12>
        <div class="pa-3">
          <span class="footer-title">רשימת תפוצה</span>
        </div>
        <span class="title ">הצטרף אלינו וקבל עדכונים חמים!</span>
        <v-flex xs8 mx-auto>
          <v-flex>
            <span class="txt-field">אימייל</span>
            <v-text-field
              solo
              dense
              placeholder="info@gmail.com"
            ></v-text-field>
          </v-flex>
        </v-flex>
      </v-flex>
      <v-flex text-center  lg3 sm6 xs12>
        <div class="pa-3">
          <span class="footer-title">צור קשר</span>
        </div>
        <span>Office@Psychostaion.co.il</span><br />
        <span>+972 54 222 6 845</span>
      </v-flex>
      <v-flex text-center  lg3 sm6 xs12>
        <div class="pa-3">
          <span class="footer-title">צור קשר</span>
        </div>
        <v-flex>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-flex>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ['mdi-instagram', 'mdi-youtube', 'mdi-facebook'],
    menu: [
      { title: 'טופ 10', page: '/top10' },
      { title: 'רישמת תחנות', page: '/radio' },
      { title: 'פלייליסטים', page: '/playlists' },
      { title: 'אירועים', page: '/events' },
      { title: 'חדשות', page: '/news' },
      { title: 'תרומות', page: '/donate' }
    ]
  })
}
</script>
