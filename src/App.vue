<template>
  <div id=app>
    <h1> Twój email to: {{email}} </h1>
	<input type="text" v-model = "email">
  </div>
</template>

<script>
export default {
	data() {
		return{
			email: '',
		};
	}
	
}

</script>

<style>

</style>
