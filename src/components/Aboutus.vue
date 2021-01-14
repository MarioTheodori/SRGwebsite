<template>
    <div>            
        <div class="containscard">
            <v-img src="../assets/aboutback.png">
                <div class="cardcont">
                    <v-card class="vcard">
                        <div class="marg">
                            <v-card-text class="font">SRG Handel und Dienstleistung<br>
                                                                    is an international software services organization,<br>
                                                                    providing professional software services to clients globally.<br>
                                                                    We serve customers worldwide offering different services<br>
                                                                    and solutions with experience in the international market.<br>
                                                                    We achieve your goals with our expertise in the<br>
                                                                    field with high efficiency and the shortest time possible.
                            </v-card-text>
                        </div>
                    </v-card>
                </div>
            </v-img>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Aboutus',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.font{
    white-space: nowrap;
    text-align: left;
    font-family: PetitaBold !important;
    color: black !important;
    align-self: center;
    font-size: 1.5vw;
    line-height: 1.5;
}
@media only screen and (min-width: 40em) { 
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
        margin-right: 5%;
        margin-top: 1%;
        margin-bottom: 1%;
        border-radius: 0% !important;
        background-color: rgba(239,239,239,1) !important;
        justify-items: center;
        align-items: center;
        overflow: auto;
    }
    .cardcont{
    display: flex;
    flex-direction: row-reverse;
    height: 100%;
    align-items: center;
    }
    .marg{
        padding: 3vw;
    }
}
@media only screen and (max-width: 40em) {
    .cardcont{
    display: grid;
    height: 100%;
    align-items: center;
    justify-items: center;
    }
    .vcard{
        display: grid;
        width: fit-content;
        height: fit-content;
        border-radius: 0% !important;
        background-color: rgba(239,239,239,1) !important;
        justify-items: center;
        align-items: center;
    }
    .marg{
        padding: 1vw;
    }
 }
</style>
