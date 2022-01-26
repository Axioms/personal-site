<template>
  <article class="bg-white dark:bg-gray-900 rounded-lg px-6 py-8 ring-1 ring-gray-900/5 shadow-xl m-3.5 mx-auto hover:shadow-2xl hover:animate-pulse">
    <h1 class="p-1.5 mb-4 text-4xl dark:text-gray-100 border-b" >{{ page.title }}</h1>
    <nuxt-content class="dark:text-gray-100" :document="page"/>
  </article>
</template>

<script>
export default {
  async fetch() {``
    this.page = await this.$content('hello').fetch();
  },
  data() {
    return { page: null };
  }
};
/*
export default {
  async asyncData({ $content }) {
    const page = await this.$content('hello')
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Page not found' })
      })

    return {
      page
    };
  },
}
*/
</script>
