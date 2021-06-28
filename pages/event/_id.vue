<template>
	<!-- <h1>Event # {{$route.params.id}}</h1> -->
		<h1>{{event.name}}</h1>
</template>

<script>
export default {
	validate({params}) {
		// console.log(params);
		return /^\d+$/.test(params.id)
	},
	asyncData({params}) {
		return new Promise(resolve => {
			setTimeout(() => {
				resolve({
					event: {name: `Test event ${params.id}`
					}
				})
			}, 1500)
		})
	}
}
</script>