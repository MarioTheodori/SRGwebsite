<template>
    <div class="mainCont my-4">
        <div class="my-5"><span class="title text-h4">SERVICES</span></div>
        <div class="containers ma-0">
            <div class="cards">
                <v-card class="smallcard" elevation="3"><v-card-text class="font">Customized Software Development</v-card-text>
                    <v-img
                        class="ma-0 pa-0 center"
                        height="40"
                        width="40"
                        max-height="40"
                        max-width="40"
                        contain
                        src="../assets/software.png"
                    ></v-img>
                </v-card>
                <v-card class="smallcard" elevation="3"><v-card-text class="font">Software Analytics</v-card-text>
                    <v-img
                        class="ma-0 pa-0 center"
                        height="40"
                        width="40"
                        max-height="40"
                        max-width="40"
                        contain
                        src="../assets/algorithm.png"
                    ></v-img>
                </v-card>
                <v-card class="smallcard" elevation="3"><v-card-text class="font">Software Testing</v-card-text>
                    <v-img
                        class="ma-0 pa-0 center"
                        height="40"
                        width="40"
                        max-height="40"
                        max-width="40"
                        contain
                        src="../assets/test.png"
                    ></v-img>
                </v-card>
                <v-card class="smallcard" elevation="3"><v-card-text class="font">Software Solutions</v-card-text>
                    <v-img
                        class="ma-0 pa-0 center"
                        height="40"
                        width="40"
                        max-height="40"
                        max-width="40"
                        contain
                        src="../assets/puzzle.png"
                    ></v-img>
                </v-card>
            </div>
            <div class="backgroundimg">
                <v-img src="../assets/servicesback.png"></v-img>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Services',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
    font-family: PetitaMedium !important;
    color: black !important;
}
.mainCont{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0%;
    max-height: 550px;
}
.title{
    font-family: PetitaMedium !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 25px !important;
}
.smallcard{
    
    background-color: rgba(246,246,246,1) !important;
    height: 200px;
    width: 200px;
    border-radius: 0% !important;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    
}
.font{
    text-align: center;
    font-size: 17px;
}
.cards{
    grid-column: 2 / span 1;
    grid-row: 1 / 6;
    display: flex;
    justify-content:center;
    width: 85%;
    z-index: 2;
    gap: 2%;
    justify-self: center;
}
.center {
    align-self: center !important;
}
.containers{
    width: 100% !important;
    display: grid;
    grid-template-columns: 15% 70% 15%;
    grid-template-rows: auto auto auto auto auto auto auto auto auto auto auto auto;

}
.backgroundimg{
    grid-row: 2 / 11;
    grid-column: 2 / span 1;
}
</style>
