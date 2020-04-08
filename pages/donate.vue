<template>
  <div>
    <v-layout wrap justify-center style="height:800px;">
      <v-flex
        xs12
        class="main title-container elevation-6 d-flex align-center justify-right"
      >
        <v-flex>
          <span class="sitetitle">תרמו לנו</span><br />
          <v-flex xs3 pt-2>
            <v-divider class="divider"></v-divider>
          </v-flex>
        </v-flex>
      </v-flex>
      <v-flex xs10>
        <div class="svgs-index-block" style="top:20vh;">
          <img
            class="svg"
            src="fill/pink-el.svg"
            style="left: 6vh; top: 10vh;"
          />
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

        <v-flex pa-5 xl8 xs12>
          <p>
            טראנסנטר הוא אתר חינמי, עזור לנו להשאיר אותו כך, עם כמות צפיות העולה
            כל הזמן אנו זקוקים כל הזמן .לעלות את כמות המשאבים שלנו
          </p>
          <p>
            אנחנו נמשיך לתחזק ולהביא לכם את המוזיקה הכי חמה בשוק ולעלות את כמות
            התחנות ובעתיד גם .אפליקציות למובייל. אבל כדי לעשות את כל זה אנחנו
            זקוקים לעזרתכם
          </p>
        </v-flex>
        <v-flex lg3 xs12 pt-5>
          <v-btn
            block
            @click="dialog = true"
            rounded
            text
            class="signup-btn"
            large
          >
            תרום עכשיו</v-btn
          >
        </v-flex>
      </v-flex>
    </v-layout>
    <v-dialog v-model="dialog" max-width="900" max-height="800">
      <v-container dark>
        <v-flex xs12 text-center>
          <span class="sitetitle dialog">תרמו לנו</span>
        </v-flex>
        <v-layout wrap ma-5>
          <v-flex text-right>
            <span class="subtitle">תרמו בעזרת:</span>
          </v-flex>
          <v-flex xs12>
            <v-layout wrap ma-5>
              <v-flex xs4>
                <v-card max-width="236">
                  <v-img src="photos/barcode.jpg"></v-img>
                </v-card>
              </v-flex>
              <v-flex xs8 text-left align-left>
                <span>bitcoin</span><br />
                <span ref="address">{{ address }}</span
                ><br />
                <input type="hidden" id="address" :value="address" />
                <v-btn :elevation="1">
                  <v-flex @click="Copy()" align-end
                    ><v-img class="copy-icon" src="icons/copy.svg"></v-img
                    ><span> Click to Copy</span></v-flex
                  >
                </v-btn>
              </v-flex>
            </v-layout>
            <v-layout wrap ma-5>
              <v-flex xs4>
                <v-card max-width="236">
                  <v-img src="photos/barcode.jpg"></v-img>
                </v-card>
              </v-flex>
              <v-flex xs8 text-left align-left>
                <span>bitcoin</span><br />
                <span>{{ address }}</span
                ><br />
                <input type="hidden" id="address" :value="address" />
                <v-btn :elevation="1">
                  <v-flex @click="Copy()" align-end
                    ><v-img class="copy-icon" src="icons/copy.svg"></v-img
                    ><span> Click to Copy</span></v-flex
                  >
                </v-btn>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-container>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      address: '1EkiAuTkBa1VSvTrWhEhstq8phaAetYZa1'
    }
  },
  methods: {
    Copy() {
      let testingCodeToCopy = document.querySelector('#address')
      testingCodeToCopy.setAttribute('type', 'text') // 不是 hidden 才能複製
      testingCodeToCopy.select()

      try {
        var successful = document.execCommand('copy')
        var msg = successful ? 'successful' : 'unsuccessful'
        alert('address was copied ' + msg)
      } catch (err) {
        alert('Oops, unable to copy')
      }

      /* unselect the range */
      testingCodeToCopy.setAttribute('type', 'hidden')
      window.getSelection().removeAllRanges()
    }
  }
}
</script>

<style lang="scss" scoped>
p {
  font-family: Anomalia-regular !important;
  font-size: 1.3rem;
}
.copy-icon {
  height: 22px;
  width: 18px;
  display: inline-flex;
  margin-right: 10px;
  float: left;
}
.container {
  background: #042954;
}
.theme--dark.v-btn:not(.v-btn--flat):not(.v-btn--text):not(.v-btn--outlined) {
  background: #ffffff0a !important;
  padding-right: 3%;
  padding-left: 3%;
  display: inline;
}
.dialog.sitetitle:after {
  content: '';
  display: block;
  height: 0.2em;
  width: 5%;
  margin: auto;
  border-bottom: solid #4bcfad;
}
</style>
