<template>
    <div>            
        <div class="containscard">
            <v-img src="../assets/aboutback.png">
                <div class="cardcont">
                    <v-card class="vcard">
                        <div class="marg">
                            <v-card-text class="font pa-0 pb-md-1 text-md-body-1 text-caption">SRG Handel und Dienstleistung</v-card-text>
                            <v-card-text class="font pa-0 pb-md-1 text-md-body-1 text-caption">is an international software services organization,</v-card-text>
                            <v-card-text class="font pa-0 pb-md-1 text-md-body-1 text-caption">providing professional software services to clients globally.</v-card-text>
                            <v-card-text class="font pa-0 pb-md-1 text-md-body-1 text-caption">We serve customers worldwide offering different services</v-card-text>
                            <v-card-text class="font pa-0 pb-md-1 text-md-body-1 text-caption">and solutions with experience in the international market.</v-card-text>
                            <v-card-text class="font pa-0 pb-md-1 text-md-body-1 text-caption">We achieve your goals with our expertise in the</v-card-text>
                            <v-card-text class="font pa-0 text-md-body-1 text-caption">field with high efficiency and the shortest time possible.</v-card-text>
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

.vcard{
    display: grid;
    width: 46%;
    height: 83%;
    margin-right: 5%;
    margin-top: 1%;
    margin-bottom: 1%;
    border-radius: 0% !important;
    background-color: rgba(239,239,239,1) !important;
    justify-items: center;
    align-items: center;
    overflow: auto;
}
.font{
    white-space: nowrap;
    text-align: left;
    font-family: PetitaBold !important;
    color: black !important;
    align-self: center;
}
.cardcont{
    display: flex;
    flex-direction: row-reverse;
    height: 100%;
    align-items: center;
}
</style>
