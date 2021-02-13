<template>
    <div class="mainCont">
        <div class="my-3"><span class="title">SOLUTIONS</span></div>
        <div class="containers ma-0">
            <span class="fonttitle2">CMS Development</span>
            <span class="fonttitle2">BI Solution</span>
            <span class="fonttitle2">Mobile Applications</span>
        </div>
        <div class="my-4 grid-container">
            <div class="cards">
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle left">OPERATING SYSTEMS</v-card-text>
                    <div class="left">
                        <span class="font ">Microsoft Windows<br>Android<br>IOS, OS X<br>Linux, Unix</span>
                    </div>
                </v-card>
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle right">DATABASE</v-card-text>
                    <div class="right">
                        <span class="font ">Microsoft SQL Server<br>MySQL<br>Oracle<br>IMB DB2<br>Cassandra<br>MongoDB<br>mySQL<br>PostGres<br>Postgresql</span>
                    </div>
                </v-card>
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle left">PROGRAMMING LANGUAGES & FRAMEWORKS</v-card-text>
                    <div class="left">
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
.containers{
    width: 100% !important;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
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
@media only screen and (min-width: 45em) { 
    .cards{
    grid-column: 2 / 3;
    grid-row: 3 / 10;
    display: flex;
    justify-content:center;
    align-content: center;
    z-index: 2;
}
    .title{
    font-family: SpaceGrotesk !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 2.5vw !important;
}
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
    margin-right: 3%;
}
.fonttitle{
    text-align: center;
    font-size: 1.7vw;
}
.font{
    text-align: left;
    font-size: 1.5vw;
    white-space: normal;
}
}
@media only screen and (max-width: 45em) {
    .left{
        grid-column: 2 / 3;
        justify-self: left;
        text-align: left;
        margin-bottom: 10px;
    }
    .right{
        grid-column: 2 / 3;
        justify-self: right;
        text-align: right;
        margin-bottom: 10px;
    }
    .cards{
    grid-column: 1 / -1;
    grid-row: 1 / -1;
    display: flex;
    flex-direction: column;
    justify-content:center;
    align-content: center;
    z-index: 2;
}
    .title{
    font-family: SpaceGrotesk !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 24px !important;
} 
    .backgroundimg{
    display: none;
    }
    .smallcard{
    height: fit-content;
    background-color: rgba(246,246,246,1) !important;
    border-radius: 0% !important;
    display: grid;
    grid-template-columns: 10% 80% 10%;
    overflow:auto;
    margin-right: 3%;
    margin-bottom: 20px;
    }
    .fonttitle{
        font-size: 16px;
        font-weight: 550;
        padding: 0;
        padding-top:2px;
        padding-left: 5px;
        padding-right: 5px;
    }
    .fonttitle2{
        font-size: 16px;
        padding: 0;
        padding-top:2px;
        padding-left: 5px;
        padding-right: 5px;
    }
    .font{
        font-size: 14px;
        white-space:normal;
    }
}
</style>

