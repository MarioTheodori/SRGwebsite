<template>
    <div class="mainCont my-4">
        <div class="my-5"><span class="title text-h4">SOLUTIONS</span></div>
        <div class="containers ma-0 my-8">
            <span class="font2">CMS Development</span>
            <span class="font2">BI Solution</span>
            <span class="font2">Mobile Applications</span>
        </div>
        <div class="my-4 grid-container">
            <div class="cards">
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle">OPERATING SYSTEMS</v-card-text>
                    <div class="ma-0 pa-0 pb-4">
                        <span class="font">Microsoft Windows<br>Android<br>IOS, OS X<br>Linux, Unix</span>
                    </div>
                </v-card>
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle">DATABASE</v-card-text>
                    <div class="ma-0 pa-0 pb-4">
                        <span class="font">Microsoft SQL Server<br>MySQL<br>Oracle<br>IMB DB2<br>Cassandra<br>MongoDB<br>mySQL<br>PostGres<br>Postgresql</span>
                    </div>
                </v-card>
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle px-1">PROGRAMMING LANGUAGES & FRAMEWORKS</v-card-text>
                    <div class="ma-0 pa-0 pb-4">
                        <span class="font">Microsoft, .Net,<br> ASP.Net, ASP Classic,<br> C#, Java,<br> Visual BASIC, PHP,<br> C, C++,<br> elixir, Xamarin,<br> Laravel, Dot,<br> Net Core, Sharepoint,<br> Ms, Dynamics CRM,<br> HTML5, AngularJS,<br> CSS3, JavaScript,<br> jQuery, PhoneGap,<br> Bootstrap, Nodejs</span>
                    </div>
                </v-card>
            </div>
            <div class="backgroundimg">
                <v-img src="../assets/solutions.png"></v-img>
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
}
.title{
    font-family: PetitaMedium !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 2.5vw !important;
}
.containers{
    width: 100% !important;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.cards{
    grid-column: 2 / 3;
    grid-row: 3 / 10;
    display: flex;
    justify-content:center;
    align-content: center;
    gap: 4%;
    z-index: 2;
}
.padfix{
    padding-left: 42px;
    padding-right: 41px;
}
.grid-container{
    width: 100%;
    display: grid;
    grid-template-columns: 10% 80% 10%;
    grid-template-rows: 20px repeat(10, 1fr) 1px;
}
.font2{
    text-align: center;
    font-size: 1.5vw;
    font-family: PetitaBold !important;
}
@media only screen and (min-width: 40em) { 
    .backgroundimg{
    grid-row: 2 / -1;
    grid-column: 2 / 3;
}
    .smallcard{
    height: fit-content;
    background-color: rgba(246,246,246,1) !important;
    width: 23vw;
    max-height: 60vw;
    border-radius: 0% !important;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.fonttitle{
    text-align: center;
    font-size: 1.5vw;
    font-family: PetitaBold !important;
}
.font{
    text-align: left;
    font-size: 1.3vw;
    font-family: PetitaLight !important;
    white-space: normal;
}
}
@media only screen and (max-width: 40em) { 
    .backgroundimg{
    grid-row: 1 / -1;
    grid-column: 1 / -1;
    }
    .smallcard{
    height: fit-content;
    background-color: rgba(246,246,246,1) !important;
    width: 20vw;
    max-height: 70vh;
    border-radius: 0% !important;
    display: flex;
    flex-direction: column;
    align-items: center;
    overflow:auto;
    }
    .fonttitle{
        text-align: center;
        font-size: 1.5vw;
        font-family: PetitaBold !important;
        padding: 0;
        padding-top:2px;
        padding-left: 5px;
        padding-right: 5px;
    }
    .font{
        text-align: left;
        font-size: 1.3vw;
        font-family: PetitaLight !important;
        white-space:normal;
    }
}
</style>

