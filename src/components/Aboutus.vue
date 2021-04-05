<template>
    <div class="containers">            
        <div class="containscard">
            <img class="hide" src="../assets/aboutback.png" alt="">
        </div>
        <v-card class="vcard">
            <div class="marg">
                <v-card-text class="font topm">SRG Handel und Dienstleistung</v-card-text>
                <v-card-text class="font botm">
                    {{text}}
                </v-card-text>
            </div>
        </v-card>
        <div class="line1"></div>
        <div class="line2"></div>
    </div>
</template>

<script>
export default {
  name: 'Aboutus',
  props: {
      english: {
          type: Boolean,
          required: true
      }
  },
  computed: {
      text: function () {
          if (this.english) {
              return`is an international software services organization,
                    providing professional software services to clients globally.
                    We serve customers worldwide offering different services
                    and solutions with experience in the international market.
                    We achieve your goals with our expertise in the
                    field with high efficiency and the shortest time possible.`
          }
          return`ist eine internationale Software-Service-Organisation,
                die Kunden weltweit professionelle Software-Services bietet.
                Wir bedienen Kunden weltweit und bieten verschiedene Dienstleistungen 
                und Lösungen mit Erfahrung auf dem internationalen Markt.
                Wir erreichen Ihre Ziele mit unserer Fachkompetenz
                mit hoher Effizienz und kürzester Zeit.`
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
  font-family: 'Space Grotesk', sans-serif !important;
  font-size: 1.2rem;
  text-align: center;
  color: black !important;
}
@media only screen and (min-width: 45em) {
    
    /* .lines{
        grid-column: 1 / -1;
        grid-row: 1 / -1;
        z-index: 3;
        overflow: hidden;
        height: 100%;
    } */
    .line1{
        /* position: relative;
        width: 45%;
        left: 8%;
        top: 25%; */
        grid-column: 2 / 5;
        grid-row: 3 / 6;
        z-index: 3;
        height: 5px;
        background-color: red;
    }
    .line2{
        /* position: relative;
        left: 8%;
        top: 25%;
        height: 90%; */
        grid-column: 2 / 3;
        grid-row: 3 / -1;
        width: 5px;
        height: 100%;
        background-color: red;
        z-index: 3;
    }
    /* .line3{
        grid-column: 1 / 2;
        grid-row: 10 / 10;
        width: 104%;
        height: 5px;
        background-color: red;
        z-index: 3;
    } */
    .topm{
        padding-bottom: 0;
        margin-top: 20px;
        font-weight: 600 !important;
    }
    .botm{
        padding-top: 0;
        margin-bottom: 20px;
    }
    .hide{
        width: 100%;
        max-height: 100%
    }
    .containscard{
        grid-column: 1 / 12;
        grid-row: 1 / -1;
        z-index: 0;
        height: 100%;
        width: 100%;
    }
    .containers{
        width: 100%;
        display: grid;
        grid-template-columns: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
        grid-template-rows: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
    }
    .font{
    text-align: justify;
    color: black !important;
    align-self: center;
    font-size: 1.5vw;
    line-height: 1.5;
    }
    .cardcont{
    display: flex;
    flex-direction: row-reverse;
    height: 100%;
    align-items: center;
    }
    .vcard{
        display: grid;
        width: fit-content;
        height: fit-content;
        border-radius: 0% !important;
        background-color: rgba(239,239,239,1) !important;
        justify-items: center;
        align-items: center;
        grid-row: 2 / 7;
        grid-column: 4 / 10;
        z-index: 2;
    }
    .cardcont{
    display: flex;
    flex-direction: row-reverse;
    height: 100%;
    align-items: center;
    }
    .marg{
        margin: 4.5vw;
    }
}
@media only screen and (max-width: 45em) {
    .line1{
        position: relative;
        width: 5px;
        z-index: 1;
        height: 110%;
        left: 20px;
        background-color: red;
    }
    .hide{
        display: none;
    }
    .containers{
        width: 100%;
        display: grid;
        grid-template-columns: 3% auto 3%;
        grid-template-rows:  20px 1fr 1fr;
    }
    .containscard{
        background-image: url(../assets/aboutback.png);
        background-repeat: no-repeat;
        grid-column: 1 / -1;
        grid-row: 1 / 3;
        z-index: 0;        
    }
    .topm{
        padding-bottom: 0;
        margin-top: 20px;
        font-weight: 600;
    }
    .botm{
        padding-top: 0;
        margin-bottom: 20px;
    }
    .font{
    text-align: left;
    color: black !important;
    align-self: center;
    font-size: 18px;
    line-height: 2;
    padding-left: 50px;
    padding-right: 50px;
    }
    .vcard{
        display: grid;
        height: fit-content;
        border-radius: 0% !important;
        background-color: rgba(239,239,239,1) !important;
        justify-items: center;
        align-items: center;
        grid-column: 2 / 3;
        grid-row: 2 / 4;
        z-index: 2;
    }
    .marg{
        padding: 0vw;
    }
 }
</style>
