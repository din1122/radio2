<template>
  <div>
    <v-layout wrap justify-center>
      <v-flex xs8 d-block>
        <v-img
          src="events/festival1.jpg"
          max-height="300"
          position="end"
        ></v-img>
      </v-flex>
      <!--
      <v-flex
        xs8
        class="main title-container elevation-6 d-flex align-center justify-right"
      >
        <v-card>
          <v-img src="events/festival1.jpg" contain></v-img>
        </v-card>
      </v-flex>
      -->
      <v-flex xs8 pa-5>
        <v-container>
          <div class="container-svg">
            <img class="svg" src="fill/side-el.svg" />
            <img class="svg" src="fill/side-el1.svg" style="top:100px;" />
            <img class="svg" src="fill/side-el2.svg" style="top:140px;" />
          </div>
          <v-layout wrap>
            <v-flex xs12 pb-3 class="subtitle-box">
              <span class=" stations-text">כותרת כתבה</span>
            </v-flex>
            <v-flex xs12>
              <p>
                לורם איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום
                דולור סיט אמט, מוסן מנת. להאמית קרהשק סכעיט דז מא, מנכם למטכין
                נשואי מנורך. קולהע צופעט למרקוח איבן איף, ברומץ כלרשט מיחוצים.
                קלאצי ושבעגט ליבם סולגק. בראיט ולחת צורק מונחף, בגורמי מגמש.
                תרבנך וסתעד לכנו סתשם השמה - לתכי מורגם בורק? לתיג ישבעס. לורם
                איפסום דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור
                סיט אמט, מוסן מנת. להאמית קרהשק סכעיט דז מא, מנכם למטכין נשואי
                מנורך. קולהע צופעט למרקוח איבן איף, ברומץ כלרשט מיחוצים. קלאצי
                ושבעגט ליבם סולגק. בראיט ולחת צורק מונחף, בגורמי מגמש. תרבנך
                וסתעד לכנו סתשם השמה - לתכי מורגם בורק? לתיג ישבעס. לורם איפסום
                דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט
                אמט, מוסן מנת. להאמית קרהשק סכעיט דז מא, מנכם למטכין נשואי
                מנורך. קולהע צופעט למרקוח איבן איף, ברומץ כלרשט מיחוצים. קלאצי
                ושבעגט ליבם סולגק. בראיט ולחת צורק מונחף, בגורמי מגמש. תרבנך
                וסתעד לכנו סתשם השמה - לתכי מורגם בורק? לתיג ישבעס. לורם איפסום
                דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט
                אמט, מוסן מנת. להאמית קרהשק סכעיט דז מא, מנכם למטכין נשואי
                מנורך. קולהע צופעט למרקוח איבן איף, ברומץ כלרשט מיחוצים. קלאצי
                ושבעגט ליבם סולגק. בראיט ולחת צורק מונחף, בגורמי מגמש. תרבנך
                וסתעד לכנו סתשם השמה - לתכי מורגם בורק? לתיג ישבעס. לורם איפסום
                דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט
                אמט, מוסן מנת. להאמית קרהשק סכעיט דז מא, מנכם למטכין נשואי
                מנורך. קולהע צופעט למרקוח איבן איף, ברומץ כלרשט מיחוצים. קלאצי
                ושבעגט ליבם סולגק. בראיט ולחת צורק מונחף, בגורמי מגמש. תרבנך
                וסתעד לכנו סתשם השמה - לתכי מורגם בורק? לתיג ישבעס. לורם איפסום
                דולור סיט אמט, קונסקטורר אדיפיסינג אלית לורם איפסום דולור סיט
                אמט, מוסן מנת. להאמית קרהשק סכעיט דז מא, מנכם למטכין נשואי
                מנורך. קולהע צופעט למרקוח איבן איף, ברומץ כלרשט מיחוצים. קלאצי
                ושבעגט ליבם סולגק. בראיט ולחת צורק מונחף, בגורמי מגמש. תרבנך
                וסתעד לכנו סתשם השמה - לתכי מורגם בורק? לתיג ישבעס.
              </p>
            </v-flex>
            <v-flex>
              <v-flex xs4>
                <v-text-field label="אימייל" solo></v-text-field>
              </v-flex>
            </v-flex>
            <v-flex xs12>
              <v-flex xs3>
                <v-textarea label="תגובה" solo></v-textarea>
              </v-flex>
            </v-flex>
            <v-flex>
              <v-btn rounded class="Readmore">שלח</v-btn>
            </v-flex>
          </v-layout>
        </v-container>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  data() {
    return {
      desc: ''
    }
  }
}
</script>

<style lang="scss">
.theme--dark.v-text-field--solo > .v-input__control > .v-input__slot {
  border: 1px solid #4bcfad;
}
</style>
