<template>
    <div class="mainCont my-4">
        <div class="my-5"><span class="title text-h4">SOLUTIONS</span></div>
        <div class="containers ma-0 my-8">
            <span>CMS Development</span>
            <span>BI Solution</span>
            <span>Mobile Applications</span>
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
                    <div class="ma-0 pa-0 pb-4 px-10">
                        <span class="font">Microsoft .Net, ASP.Net<br>ASP Classic, C#<br>Java, Visual BASIC<br>PHP,C,C++,elixir<br>Xamarin, Laravel, Dot<br>Net Core<br>Sharepoint, Ms<br>Dynamics CRM, HTML5, AngularJS<br>CSS3, JavaScript<br>jQuery<br>PhoneGap, Bootstrap<br>Node,js</span>
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
    font-size: 25px !important;
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
.smallcard{
    height: fit-content;
    background-color: rgba(246,246,246,1) !important;
    width: fit-content;
    min-width: 240px;
    max-width: 250px;
    border-radius: 0% !important;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.fonttitle,span{
    text-align: center;
    font-size: 16px;
    font-family: PetitaBold !important;
}
.font{
    text-align: left;
    font-size: 15px;
    font-family: PetitaLight !important;
}
.padfix{
    padding-left: 42px;
    padding-right: 41px;
}
.grid-container{
    display: grid;
    grid-template-columns: 20% 60% 20%;
    grid-template-rows: 20px repeat(10, 1fr) 1px;
}
.backgroundimg{
    grid-row: 2 / -1;
    grid-column: 2 / 3;
}
</style>

