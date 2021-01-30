<template>
    <div>            
        <div class="containers">
            <v-img class="py-5 img" src="../assets/contactus.png">
                <div class="containers test">
                    <v-card class="maincard" elevation="5">
                        <v-card-title class="title">CONTACT US</v-card-title>
                        <v-form ref="form" @submit.prevent="sendEmail" class="pa-10">
                                <v-text-field
                                    name="user_name"
                                    type="text"
                                    label="Name"
                                    required
                                    ></v-text-field>
                                    <v-text-field
                                    type="email"
                                    name="user_email"
                                    label="E-mail"
                                    required
                                ></v-text-field>
                                <v-text-field
                                    label="Phone"
                                    type="phone"
                                    name="user_phone"
                                    required
                                ></v-text-field>
                                <v-text-field
                                    label="Subject"
                                    name="subject"
                                    type="text"
                                    required
                                ></v-text-field>
                                <v-textarea
                                    label="Message"
                                    name="message"
                                    required
                                ></v-textarea>
                                <div class="right">
                                    <v-btn
                                    class="mr-4"
                                    type="submit"
                                    style="font-family: PetitaMedium;"
                                    >Submit</v-btn>
                                </div>
                        </v-form>
                    </v-card>
                    <v-card class="smallcard" elevation="3">
                        <v-card-title class="pa-0 pl-1"><img src="../assets/gmail.png" class="pr-1 fix2"><span class="pl-1">mhdd.salem@gmail.com</span></v-card-title>
                        <v-card-title class="pa-0 pl-1"><img src="../assets/telephone.png" class="pr-1 fix2"><span class="pl-1">+49 123 45678</span></v-card-title>
                    </v-card>
                </div>
            </v-img>
        </div>
    </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: 'ContactUs',
  methods: {
    sendEmail: (e) => {
      emailjs.sendForm('service_ajg291b', 'template_xet30e3', e.target, 'user_iADWPMUgkXv31zsO46tRb')
        .then((result) => {
            console.log('SUCCESS!', result.status, result.text);
        }, (error) => {
            console.log('FAILED...', error);
        });
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
    font-family: Petitamedium !important;
}
.fix2{
    height: 2vw;
    width: 2.5vw;
}
.containers{
    height: 100%;
    width: 100%;
}
.test{
    display: flex;
    flex-direction: row-reverse;
    align-content: center;
    justify-content: center;
}
.maincard{
    height: fit-content;
    width: fit-content;
    min-width: 70%;
    border-radius: 0%;
    position: relative;
    background-color: rgba(239,239,239,1) !important;
}
.smallcard {
    display: grid;
    justify-content: center;
    align-content: center;
    min-width: fit-content;
    min-height: fit-content;
    gap: 5%;
    height: 25vw;
    width: 22vw;
    border-radius: 0%;
    background-color:rgba(220,0,45,1);
    align-self: center;
    position: relative;
    bottom: 60px;
}

.img{
    padding-top: 20px;
}
img{
    height: 25px;
    width: 25px;
}
.right{
    display: flex;
    flex-direction: row-reverse;
}
@media only screen and (max-width: 45em) {
    .title{
        font-family: PetitaBold !important;
        font-weight: 520 !important;
        font-size: 5vw !important;
        justify-content: center;
    }
    span{
    font-family: PetitaMedium;
    color: white !important;
    font-size: 2.5vw;
    }
    .smallcard{
        display: none;
    }
}
@media only screen and (min-width: 45em) {
    .title{
    font-family: PetitaBold !important;
    font-weight: 520 !important;
    font-size: 2.5vw !important;
    justify-content: center;
    }
    span{
    font-family: PetitaMedium;
    color: white !important;
    font-size: 1.2vw;
    }
}
</style>
