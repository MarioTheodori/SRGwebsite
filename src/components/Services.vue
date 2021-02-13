<template>
    <div class="mainCont my-4">
        <div class="my-5"><span class="title">SERVICES</span></div>
        <div class="containers ma-0">
            <div class="cards">
                <v-card class="smallcard" elevation="0"><v-card-text class="font fix1">Customized Software Development</v-card-text>
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
                <v-card class="smallcard" elevation="0"><v-card-text class="font">Software Analytics</v-card-text>
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
                <v-card class="smallcard" elevation="0"><v-card-text class="font">Software Testing</v-card-text>
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
                <v-card class="smallcard" elevation="0"><v-card-text class="font">Software Solutions</v-card-text>
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
                <v-img src="../assets/servicesback.png" class="hide"></v-img>
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
    color: black !important;
}
.mainCont{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0%;
    max-height: 550px;
}

.center {
    align-self: center !important;
}


@media only screen and (max-width: 45em) {
    .containers{
    width: 100% !important;
    display: grid;
    grid-template-columns: 20% 60% 20%;
    grid-template-rows: auto auto auto auto auto auto;

    }
    .cards{
    grid-column: 2 / span 1;
    grid-row: 1 / 5;
    display: flex;
    flex-direction: column;
    height: fit-content;
    flex-wrap: wrap;
    justify-content:center;
    width: 100%;
    z-index: 2;
    justify-self: center;
    margin-bottom: 15px;
    margin-left: 20px;
    }
    .title{
    font-family: SpaceGrotesk !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 24px !important;
    }
    .font{
        text-align: center;
        font-size: 16px;
        white-space:normal;
        text-align: left;
    }
    .backgroundimg{
    grid-row: 5 / -1;
    grid-column: 1 / -1;
    background-image: url("../assets/servicesback.png");
    background-size: cover;
    }
    .smallcard{
    margin-top: 10px;
    min-height: fit-content;
    border-radius: 0% !important;
    display: flex;
    flex-direction: row-reverse;
    justify-content: center;
    margin-right: 2%;
}

}
@media only screen and (min-width: 45em) { 
    .containers{
    width: 100% !important;
    display: grid;
    grid-template-columns: 10% 80% 10%;
    grid-template-rows: auto auto auto auto auto auto auto auto auto auto auto auto;

}
    .cards{
    grid-column: 2 / span 1;
    grid-row: 1 / 8;
    display: flex;
    height: fit-content;
    flex-wrap: wrap;
    justify-content:center;
    width: 100%;
    z-index: 2;
    justify-self: center;
    }
    .backgroundimg{
    grid-row: 2 / 11;
    grid-column: 2 / span 1;
    }
    .smallcard{
    background-color: rgba(246,246,246,1) !important;
    min-height: fit-content;
    height: 20vw;
    width: 15vw;
    border-radius: 0% !important;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    margin-right: 2%;
    }
    .title{
    font-family: SpaceGrotesk !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 2.5vw !important;
    }
    .font{
        text-align: center;
        font-size: 1.5vw;
        line-height: 1;
    }
}
</style>
