<template>
<div class="grids">
    <div class="line1"></div>
    <div class="line2"></div>
    <div class="line3"></div>
    <div class="over"><span class="title">{{title}}</span></div>
    <div class="mainCont my-4">
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
</div>
</template>

<script>
export default {
  name: 'Services',
  props: {
      english: {
          type: Boolean,
          required: true
      }
  },
  computed: {
      title: function () {
          if (this.english) {
              return`Services`
          }
          return`Dienstleistungen`
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
    color: black !important;
}
.center {
    align-self: center !important;
}
@media only screen and (max-width: 45em) {
    .grids{
        position: relative;
        height: 100%;
        width: 100%;
    }
    .line1{
        position: absolute;
        width: 5px;
        z-index: 3;
        height: 100%;
        left: 20px;
        background-color: red;
    }
    .over{
        display: grid;
        margin-top: 10px;
    }
    .mainCont{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0%;
    max-height: 550px;
    }
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
    font-family: 'Space Grotesk', sans-serif !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 24px !important;
    align-self: center;
    justify-self: center;
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
    z-index: 4;
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
    .hide{
        height: 100%;
        width: 100%;
    }
    .over{    
        grid-column: 5 / 7;
        grid-row: 1 / 3;
        z-index: 3;
        align-self: center;
        background-color: white;
        width: fit-content;
        justify-self: center;
    }
    .mainCont{
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 0%;
        grid-column: 1 / 11;
        grid-row: 3 / 11;
    }
    .grids{
        width: 100%;
        height: fit-content;
        display: grid;
        grid-template-columns: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
        grid-template-rows: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
    }
    .line1{
        grid-column: 2 / 2;
        grid-row: 1 / 1;
        z-index: 3;
        height: 100%;
        width: 5px;
        background-color: red;
    }
     .line2{
        grid-column: 2 / 9;
        grid-row: 2 / 2;
        width: 100%;
        height: 5px;
        background-color: red;
        z-index: 1;
    }
    .line3{
        grid-column: 8 / 8;
        grid-row: 2 / -1;
        width: 5px;
        height: 100%;
        background-color: red;
        justify-self: end;
        z-index: 1;  
    }
    .containers{
    width: 100% !important;
    height: 100%;
    display: grid;
    grid-template-columns: 10% 80% 10%;
    grid-template-rows: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
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
    grid-row: 2 / -1;
    grid-column: 2 / 3;
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
    align-self: center;
    font-family: 'Space Grotesk', sans-serif !important;
    white-space: nowrap;
    font-weight: 550;
    text-align: center;
    font-style: normal;
    font-size: 2.5vw !important;
    margin-left: 3px;
    margin-right: 3px;
    }
    .font{
        text-align: center;
        font-size: 1.5vw;
        line-height: 1;
    }
}
</style>
