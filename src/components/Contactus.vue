<template>
    <div>            
        <div class="containers">
            <v-img class="py-5 img" src="../assets/contactus.png">
                <div class="containers test">
                    <v-card class="maincard" elevation="5">
                        <v-card-title class="title">CONTACT US</v-card-title>
                        <v-form ref="form" v-model="valid" class="pa-10">
                                <v-text-field
                                    v-model="name"
                                    :counter="10"
                                    :rules="nameRules"
                                    label="Name"
                                    required
                                    ></v-text-field>
                                    <v-text-field
                                    v-model="email"
                                    :rules="emailRules"
                                    label="E-mail"
                                    required
                                ></v-text-field>
                                <v-text-field
                                    label="Phone"
                                    required
                                ></v-text-field>
                                <v-text-field
                                    label="Subject"
                                    required
                                ></v-text-field>
                                <v-textarea
                                    label="Message"
                                    required
                                ></v-textarea>
                                <div class="right">
                                    <v-btn
                                    class="mr-4"
                                    @click="submit"
                                    style="font-family: PetitaMedium;"
                                    >Submit</v-btn>
                                </div>
                        </v-form>
                    </v-card>
                    <v-card class="smallcard" elevation="3">
                        <v-card-title class="pt-1"><img src="../assets/gmail.png" class="pr-1"><span class="pl-1">mhdd.salem@gmail.com</span></v-card-title>
                        <v-card-title class="pb-1"><img src="../assets/telephone.png" class="pr-1"><span class="pl-1">+49 123 45678</span></v-card-title>
                    </v-card>
                </div>
            </v-img>
        </div>
    </div>
</template>

<script>
export default {
  name: 'ContactUs',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
    display: flex;
    flex-direction: column-reverse;
    height: 50%;
    width: 17%;
    border-radius: 0%;
    background-color:rgba(220,0,45,1);
    align-self: center;
    position: relative;
    bottom: 60px;
}
.title{
    font-family: PetitaBold !important;
    font-weight: 520 !important;
    font-size: 30px !important;
    justify-content: center;
}
.img{
    padding-top: 20px;
}
span{
    font-family: PetitaMedium;
    color: white !important;
    font-size: 15px;
}
img{
    height: 25px;
    width: 25px;
}
.right{
    display: flex;
    flex-direction: row-reverse;
}
</style>
