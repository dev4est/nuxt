<template>
  <!-- <h1>Event # {{$route.params.id}}</h1> -->
  <div class="event-header">
    <div>{{ event.date_string }}</div>
    <h1>{{ event.title }}: {{ event.title_fight }}</h1>
    <hr />
    <div>{{ event.location }}</div>
    <div>{{ event.organization }}</div>
  </div>
</template>

<script>
export default {
  head() {
    let event = this.event;
    return {
      title: `${event.seo_title}` ? `${event.seo_title}` : `${event.title}: ${event.title_fight} - SEO title template`,
      meta: [
        {
          hid: "description",
          name: "description",
          content: `${event.seo_desc}` ? `${event.seo_desc}` : `${event.title}: ${event.title_fight} - SEO description template`,
        },
      ],
    };
  },
  // validate({params}) {
  // 	// console.log(params);
  // 	return /^\d+$/.test(params.id)
  // },
  async asyncData({ params, error, $axios }) {
    try {
      const event = await $axios.$get(
        `https://my-json-server.typicode.com/dev4est/mma-demo/events/${params.id}`
      );
      return { event };
    } catch (e) {
      error(e);
    }
  },
  transition: {
    name: "my-custom-transition",
    mode: "out-in",
  },
};
</script>

<style scoped>
.event-header {
  margin-top: 30px;
}
</style>