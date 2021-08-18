<template>
	<section>
		<h1>{{pageTitle}}</h1>
		<ul>
				<li v-for="event of events" :key="event.id"> 
					<a href="#" @click.prevent="goTo(event)">
						<span>{{event.title}}</span>
						<span>Data: {{event.date_string}}</span>
						<span>Location: {{event.location}}</span>
						<span>Organization: {{event.organization}}</span>
						<span>Title fight: {{event.title_fight}}</span>
					</a>
				</li>
		</ul>
	</section>
</template>


<script>
export default {
	
	asyncData({$axios, error}) {
		return $axios.$get('https://my-json-server.typicode.com/dev4est/mma-demo/events/')
			.then(events => {
				return {
					events
				}
		})
		.catch(err => {
			error(err)
		})
	},
	data() {
		return {
			pageTitle: 'Events Page'
		}
	},
	methods: {
		goTo(event) {
			this.$router.push('/event/' + event.id)
		}
	}
}
</script>

<style scoped>
	li {
		margin-bottom: 20px;
	}
	span {
		display: block;
	}
</style>