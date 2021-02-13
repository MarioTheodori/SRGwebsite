<template>
    <div class="containers">            
        <div class="containscard">
            <img class="hide" src="../assets/aboutback.png" alt="">
        </div>
        <v-card class="vcard">
            <div class="marg">
                <v-card-text class="font topm">SRG Handel und Dienstleistung</v-card-text>
                <v-card-text class="font botm">
                                            is an international software services organization,
                                            providing professional software services to clients globally.<br>
                                            We serve customers worldwide offering different services
                                            and solutions with experience in the international market.<br>
                                            We achieve your goals with our expertise in the
                                            field with high efficiency and the shortest time possible.
                </v-card-text>
            </div>
        </v-card>
    </div>
</template>

<script>
export default {
  name: 'Aboutus',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media only screen and (min-width: 45em) { 
    .topm{
        padding-bottom: 0;
        margin-top: 20px;
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
    }
    .containers{
        width: 100%;
        display: grid;
        grid-template-columns: repeat(1fr,12);
        grid-template-rows:  10% auto 3%;
    }
    .font{
    text-align: left;
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
        grid-row: 2 / 3;
        grid-column: 7 / 11;
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
        z-index: 1;
    }
    .marg{
        padding: 0vw;
    }
 }
</style>
