<template>
<div class="grids">
    <div class="line1"></div>
    <div class="line2"></div>
    <div class="line3"></div>
    <div class="line4"></div>
    <div class="line5"></div>
    <div class="line6"></div>
    <div class="over"><span class="title">{{title}}</span></div>
    <div class="mainCont">
        <div class="containers ma-0">
            <span class="fonttitle2">CMS Development</span>
            <span class="fonttitle2">BI Solutions</span>
            <span class="fonttitle2">Mobile Applications</span>
        </div>
        <div class="my-4 grid-container">
            <div class="cards">
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle left">OPERATING SYSTEMS</v-card-text>
                    <div class="left padbot">
                        <span class="font ">Microsoft Windows<br>Android<br>IOS, OS X<br>Linux, Unix</span>
                    </div>
                </v-card>
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="right2 fonttitle">DATABASE</v-card-text>
                    <div class="right padbot">
                        <span class="font">Microsoft SQL Server<br>MySQL<br>Oracle<br>IBM DB2<br>Cassandra<br>MongoDB<br>mySQL<br>PostGres<br>Postgresql</span>
                    </div>
                </v-card>
                <v-card class="smallcard" elevation="3">
                    <v-card-text class="fonttitle left">PROGRAMMING LANGUAGES & FRAMEWORKS</v-card-text>
                    <div class="left padbot">
                        <span class="font">Microsoft, .Net,<br> ASP.Net, ASP Classic,<br> C#, Java,<br> Visual BASIC, PHP,<br> C, C++,<br> elixir, Xamarin,<br> Laravel, Dot,<br> Net Core, Sharepoint,<br> Ms, Dynamics CRM,<br> HTML5, AngularJS,<br> CSS3, JavaScript,<br> jQuery, PhoneGap,<br> Bootstrap, Nodejs</span>
                    </div>
                </v-card>
            </div>
            <div class="backgroundimg">
                <v-img src="../assets/solutions.png"></v-img>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'Solutions',
  props: {
      english: {
          type: Boolean,
          required: true
      }
  },
  computed: {
      title: function () {
          if (this.english) {
              return`SOLUTIONS`
          }
          return`LÖSUNGEN`
      }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
    color: black !important;
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
    .right{
        padding-bottom: 5%;
    }
    .left{
        padding-bottom: 5%;
    }
    .line1{
        grid-column: 8 / 8;
        grid-row: 1 / 1;
        z-index: 3;
        height: 100%;
        width: 5px;
        background-color: red;
        justify-self: end;
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
         justify-self: end;
        grid-column: 1 / 1;
        grid-row: 2 / 2;
        width: 50%;
        height: 5px;
        background-color: red;
        z-index: 1;
    }
    .line4{
        justify-self: center;
        grid-column: 1 / 1;
        grid-row: 2 / 6;
        width: 5px;
        height: 100%;
        background-color: red;
        z-index: 1;
    }
    .line5{
        justify-self: end;
        align-self: flex-end;
        grid-column: 1 / 1;
        grid-row: 5 / 5;
        width: 50%;
        height: 5px;
        background-color: red;
        z-index: 1;
    }
    .line6{
        grid-column: 10 / 10;
        grid-row: 6 / 6;
        width: 100%;
        height: 5px;
        background-color: red;
        z-index: 1;
    }

    .mainCont{
        grid-column: 1 / 11;
        grid-row: 3 / 11;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 0%;
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
    .grids{
        width: 100%;
        height: fit-content;
        display: grid;
        grid-template-columns: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
        grid-template-rows: 10% 10% 10% 10% 10% 10% 10% 10% 10% 10%;
    }
    .cards{
    grid-column: 2 / 3;
    grid-row: 3 / 10;
    display: flex;
    justify-content:center;
    align-content: center;
    z-index: 2;
}
    .title{
    font-family: 'Space Grotesk', sans-serif !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 2.5vw !important;
    margin-left: 3px;
    margin-right: 3px;
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
    font-size: 1.5vw;
    line-height: 1.1;
}
.font{
    text-align: left;
    font-size: 1.3vw;
    white-space: normal;
}
    .fonttitle2{
        font-size: 20px;
        padding: 0;
        padding-top:2px;
        padding-left: 5px;
        padding-right: 5px;
    }
}
@media only screen and (max-width: 45em) {
    .padbot{
        padding-bottom: 3%;
    }
    .grids{
        position: relative;
        height: 100%;
        width: 100%;
    }
    .line1{
        position: absolute;
        width: 5px;
        z-index: 2;
        height: 100%;
        left: 20px;
        background-color: red;
    }
    .line2{
display: none;
    }
    .over{
        display: grid;
    }
    .mainCont{
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 0%;
    }
    .left{
        margin-left: 3%;
        padding-left: 2%;
        justify-self: left;
        text-align: left;
    }
    .right{
        margin-right: 5%;
        padding-right: 2% !important;
        justify-self: right;
        text-align: right;
    }
    .right2{
        padding-right: 7% !important;
        justify-self: right;
        text-align: right;
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
    font-family: 'Space Grotesk', sans-serif !important;
    white-space: nowrap;
    text-align: left;
    font-style: normal;
    font-size: 24px !important;
    align-self: center;
    justify-self: center;
    margin-bottom: 5px;
} 
    .backgroundimg{
    display: none;
    }
    .smallcard{
    height: fit-content;
    background-color: rgba(246,246,246,1) !important;
    border-radius: 0% !important;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    margin-right: 3%;
    margin-left: 3%;
    margin-bottom: 20px;
    }
    .fonttitle{
        font-size: 16px;
        font-weight: 600;
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

