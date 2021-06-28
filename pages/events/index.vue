<template>
	<section>
		<h1>{{pageTitle}}</h1>
		<ul>
				<li v-for="event of events" :key="event"> 
					<a href="#" @click.prevent="goTo(event)">Event {{event}}</a>
				</li>
		</ul>
	</section>
</template>

<script>
export default {
	asyncData() {
		return new Promise(resolve => {
			setTimeout(() => {
				resolve({
					events: [1, 2, 3, 4, 5, 6]
					})
			}, 3000)
		})
	},
	data() {
		return {
			pageTitle: 'Events Page'
		}
	},
	methods: {
		goTo(event) {
			this.$router.push('/event/' + event)
		}
	}
}
</script>