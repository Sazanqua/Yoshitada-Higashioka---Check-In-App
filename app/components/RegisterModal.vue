<template>
    <AbsoluteLayout backgroundColor="white" height="300" width="400">
        <Label left="130" top="15" class="re2Label" text="Create Account"/>
        <Label left="130" top="15" class="re2Label" text="Create Account"/>
        <TextField v-model="input.emailAddress" left="62" top="60" class="rtextfld" hint="Email Address" />
        <TextField v-model="input.password" left="62" top="105" class="rtextfld" hint="Password" secure="true"/>
        <TextField v-model="input.confirmPassword" left="62" top="150" class="rtextfld" hint="Confirm Password" secure="true" />
        <Label left="61" top="200" class="reLabel" text="By signing up, you agree to the Terms of Service and"/>
        <Label left="161" top="215" class="reLabel" text="Privacy Policy"/>
        <Button left="82" top="240" class="register_button" text="CREATE ACCOUNT" @tap="registerFunc"/>
    </AbsoluteLayout>
</template>

<script>

const Toast = require('nativescript-toast');

export default {
    data() {
        return {
            input: {
                    emailAddress: "",
                    password: "",
                    confirmPassword: ""
            }
        };
    },
    methods: {
        registerFunc(){
            this.$modal.close();
            const myToast = Toast.makeText("Created Account!");
            myToast.show();
        }
    },
}
</script>

<style>
.register_button{
    background-color: #ffc10d;
    border-radius: 48;
    color: black;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16;
    height: 41;
    width: 235;
}
.reLabel {
	color: #2699FB;
    font-size: 12;
}
.re2Label {
	color: #2699FB;
    font-size: 20;
}
.rtextfld{
    width: 275;
    border-top: #ffc10d;
    border-bottom-color: black;
    color: black;
    text-align: center;
    border-width: 1;
    background-color: white;
    font-size: 12;
}
</style>
