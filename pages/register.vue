<template>
  <v-container fluid class="forms-page">
    <div class="svg-container d-none d-sm-block">
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
          <v-flex xl3 xs10 mx-auto>
            <p class="form-title">הרשמה</p>
            <v-flex>
              <span class="txt-field">אימייל</span>
              <v-text-field solo placeholder="info@gmail.com"></v-text-field>
            </v-flex>
            <v-flex>
              <span class="txt-field">סיסמא</span>
              <v-text-field solo placeholder="************"></v-text-field>
            </v-flex>
            <v-flex>
              <span class="txt-field">אישור סיסמא</span>
              <v-text-field solo placeholder="************"></v-text-field>
            </v-flex>
            <span>בלחיצה על הירשם אתה מסכים ל</span><a href="">תנאי השימוש.</a>
            <v-flex pa-3>
              <v-btn block rounded text class="signup-btn" large>הירשם</v-btn>
            </v-flex>
            <v-flex pa-3 xs6 mx-auto>
              <v-divider class="divider"></v-divider>
            </v-flex>
            <span>יש לך משתמש? להתחברות לחץ </span
            ><nuxt-link to="/login">כאן.</nuxt-link>
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
