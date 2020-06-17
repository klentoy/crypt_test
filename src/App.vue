<template>
	<div id="app">
		<div></div>
	</div>
</template>

<script>
	import axios from 'axios';

	export default {
		name: 'App',
		components: {

		},
		mounted() {
			let API_KEY = "aef4f429-565b-41e6-9c96-1b8cf33d1612";
			axios
				.get('https://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/latest?CMC_PRO_API_KEY=aef4f429-565b-41e6-9c96-1b8cf33d1612')
				.then(response => (this.info = response))
		}
	}
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
