<template>
  <v-container fluid class="forms-page">
    <div class="svg-container svg-container d-none d-sm-block">
      <div class="pink-box svg">
        <img class="svg" src="fill/pink-el.svg" />
        <img
          class="svg"
          src="fill/cyan-l.svg"
          style="top: 62px; right: -26px;"
        />
      </div>
      <div class="cyan-box svg">
        <img
          class="svg"
          src="fill/pink-l.svg"
          style="right: -100px; top: -7px;"
        />
        <img class="svg" src="fill/cyan-el.svg" style="height:300px;" />
      </div>
    </div>
    <v-layout wrap justify-center align-center style="height:715px">
      <v-flex text-center xs12 lg4>
        <v-layout row wrap justify-space-between>
          <v-flex xs10 xl3 mr-auto ml-auto>
            <p class="form-title">התחברות</p>
            <v-flex>
              <span class="txt-field">אימייל</span>
              <v-text-field
                solo
                dense
                placeholder="info@gmail.com"
              ></v-text-field>
            </v-flex>
            <v-flex>
              <span class="txt-field">סיסמא</span>
              <v-text-field
                solo
                placeholder="**********"
                hide-details
                dense
              ></v-text-field>
            </v-flex>
            <span>
              <a class="forgot-pass" href="#">שכחת סיסמא?</a>
            </span>
            <v-flex pa-3>
              <v-btn block rounded text class="signup-btn" large>התחבר</v-btn>
            </v-flex>
            <v-flex pa-3 xs6 mx-auto>
              <v-divider class="divider"></v-divider>
            </v-flex>
            <span>משתמש חדש? להרשם לחץ</span>
            <nuxt-link to="/register">כאן.</nuxt-link>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
a {
  text-decoration: none;
  color: #4bcfad !important;
  font-family: Anomalia-medium !important;
  transition: 0.2s;
}
a:hover {
  color: #bbffed !important;
  transition: 0.2s;
}
.forgot-pass {
  color: #4bcfad;
  opacity: 0.4;
  padding: 3%;
  float: left;
  transition: 0.1s;
}
.forgot-pass:hover {
  opacity: 1;
  transition: 0.1s;
}
.cyan-box {
  right: -40px;
  bottom: 492px;
}
.pink-box {
  left: 101px;
  top: 20%;
}
</style>
