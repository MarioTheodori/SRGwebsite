<template>
    <div class="grids">
        <div class="line1"></div>     
        <div class="line2"></div>     
        <div class="containers">
            <v-img class="img" src="../assets/contactus.png">
                <div class="containers test">
                    <v-card class="maincard" elevation="0">
                        <v-card-title class="title">{{title}}</v-card-title>
                        <v-card class="redcard" elevation="3">
                            <v-card-title class="pa-0 pl-1"><img src="../assets/gmail.png" class="pr-1 fix2"><span class="pl-1 title">info@srg-tech.com</span></v-card-title>
                        </v-card>   
                        <div class="pa-10">
                            <v-form
                                class="gridss"
                                ref="form"
                                v-model="valid"
                                lazy-validation
                            >
                                <v-text-field
                                v-model="name"
                                :counter="10"
                                :rules="nameRules"
                                :label= names
                                name="user_name"
                                required
                                ></v-text-field>
                                <v-text-field
                                v-model="email"
                                :rules="emailRules"
                                label="E-mail *"
                                name="user_email"
                                required
                                ></v-text-field>

                                <v-text-field
                                :label= tele
                                type="phone"
                                v-model="phone"
                                name="user_phone"
                                ></v-text-field>
                                <v-text-field
                                    :label= subjects
                                    name="subject"
                                    v-model="subject"
                                    type="text"
                                ></v-text-field>
                                <v-textarea
                                    :label= messages
                                    name="message"
                                    v-model="message"
                                    :rules="messageRules"
                                    required
                                ></v-textarea>    
                                <v-btn
                                class="mr-4 btn"
                                @click="validate"
                                >
                                {{senden}}
                                </v-btn>
                            </v-form>
                        </div>
                    </v-card>
                    <v-card class="smallcard hide" elevation="3">
                        <v-card-title class="pa-0 pl-1"><img src="../assets/gmail.png" class="pr-1 fix2"><span class="pl-1">info@srg-tech.com</span></v-card-title>
                    </v-card>
                </div>
            </v-img>
        </div>
        <v-dialog
            v-model="dialog"
            width="500"
            >
            <v-card>
                <v-card-title class="headline lighten-2 redline">
                Thank you!
                </v-card-title>
                <v-card-text>
                {{feedback}}
                </v-card-text>
                <v-divider></v-divider>
                <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    @click="dialog = false"
                >
                    close
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  name: 'ContactUs',
  props: {
      english: {
          type: Boolean,
          required: true
      }
  },
  computed: {
      title: function () {
          if (this.english) {
              return`CONTACT US`
          }
          return`KONTAKT`
      },
        names: function () {
          if (this.english) {
              return`Name *`
          }
          return`Ihr Name *`
      },
        messages: function () {
          if (this.english) {
              return`Message *`
          }
          return`Ihre Nachricht`
      },
        tele: function () {
          if (this.english) {
              return`Phone`
          }
          return`Ihre Telefon`
      },
        senden: function () {
          if (this.english) {
              return`Submit`
          }
          return`Senden`
      },
        subjects: function () {
          if (this.english) {
              return`Subject`
          }
          return`Betreff`
      }
  },
    data: () => ({
      valid: true,
      feedback: "",
      dialog: false,
      name: '',
      phone: '',
      subject: '',
      nameRules: [
        v => !!v || 'Name is required',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      message: '',
      messageRules: [
        v => !!v || 'Message is required',
      ]
    }),
    methods: {
      validate () {
        let  templateParams = {
            user_name: this.name,
            user_email: this.email,
            user_phone: this.phone,
            user_subject: this.subject,
            user_message: this.message
          }
        console.log(this.$refs.form.validate());
        this.$refs.form.validate()
        if(this.$refs.form.validate()){
            emailjs.send('service_neeb9kq', 'template_ap8u45n', templateParams, 'user_JBaPN7atg1zx0DWAoXtIA')
            .then((result) => {
                console.log('SUCCESS!', result.status, result.text);
                this.$refs.form.reset();
                this.feedback = "Your E-mail has been sent! we will get back to you shortly"
                this.dialog = true;
            }, (error) => {
                console.log('FAILED...', error);
                this.feedback = "Oups! we encountered an error. Please try again"
                this.dialog = true;
            });
        }
      },
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.redline{
  border-top:5px solid red !important
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
.smallcard {
    display: grid;
    justify-content: center;
    align-content: center;
    min-width: fit-content;
    min-height: fit-content;
    height: 25vw;
    width: 22vw;
    border-radius: 0%;
    background-color:rgba(220,0,45,1);
    align-self: center;
    position: relative;
    bottom: 60px;
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
    .gridss{
        display: grid;
    }
    .btn{
        width: 70%;
        align-self: center;
        justify-self: center;
    }
    .grids{
        position: relative;
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
        top: 100%;
        position: absolute;
        width: 95%;
        z-index: 2;
        height: 5px;  
        left: 20px;
        background-color: red;
    }
    .fix2{
    height: 20px;
    width: 25px;
    margin-right: 5px;
}
    .redcard {
    display: grid;
    justify-content: center;
    align-content: center;
    height: 20vw;
    width: 100%;
    border-radius: 0%;
    background-color:red;
}
    .maincard{
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100%;
    min-width: 70%;
    border-radius: 0%;
    position: relative;
    background-color: white;
    border-color: white;
}
    .title{
        font-family: 'Space Grotesk', sans-serif !important;
        font-weight: 520 !important;
        font-size: 5vw !important;
        justify-content: center;
    }
    span{
    color: white !important;
    font-size: 2.5vw;
    }
    .hide{
        display: none;
    }
}
@media only screen and (min-width: 45em) {
    .redcard{
        display: none;
    }
    .fix2{
    height: 2vw;
    width: 2.5vw;
}
    .img{
    padding-top: 20px;
}
    .maincard{
    height: fit-content;
    width: fit-content;
    min-width: 70%;
    border-radius: 0%;
    position: relative;
    background-color: rgba(239,239,239,1) !important;
}
    .title{
    font-family: 'Space Grotesk', sans-serif !important;
    font-weight: 520 !important;
    font-size: 2.5vw !important;
    justify-content: center;
    }
    span{
    color: white !important;
    font-size: 1.2vw;
    }
}
</style>
