<template>
	<form>
		<h1>Login</h1>
		<div class="fom-group">
			<input type="text" class="form-control">
		</div>
		<div class="fom-group">
			<input type="password" class="form-control">
		</div>
		<button class="btn btn-primary">Login</button>
		<p><nuxt-link :to="'/'">BACK HOME</nuxt-link></p>
	</form>
</template>

<script>
export default {
	layout: 'empty'
}
</script>

<style scoped>
	form {
		width: 600px;
	}
	div,
	button {
		margin-bottom: 15px;
	}
</style>