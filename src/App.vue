<template>
  <div id=app>

    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <div v-if="email == ''">
      <login-form @login="logMeIn($event)" button-label="ZALOLGÓJ SIĘ"></login-form>
    </div>
    <div v-else>
      <after-login @logout="logOut" :email="email"></after-login>
    </div>
  </div>
</template>

<script>
import "milligram";
import LoginForm from"./LoginForm";
import AfterLogin from "./AfterLogin";
export default {
  components: {LoginForm, AfterLogin},
	data() {
		return{
			email: '',
		};
	},

  methods: {

    logMeIn(username) {
      this.email = username;
    },
    logOut() {
      this.email = '';
    }
  }
	
}

</script>

<style>

</style>
