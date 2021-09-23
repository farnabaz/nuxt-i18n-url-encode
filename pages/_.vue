<template>
  <div>
    <NuxtLink to="/en/encoded%2Furl">encoded url</NuxtLink>
    <NuxtLink to="/en/reqular/url">reqular url</NuxtLink>
    <pre>{{ route }}</pre>
  </div>
</template>

<script>
export default {
  async asyncData({ app: { i18n, localePath }, route, params, error, redirect }) {
    console.log(route);
    return {}
  },
  computed: {
    route () {
      return JSON.stringify({
        path: this.$route.path,
        params: this.$route.params,
      }, null, 2)
    }
  }
}
</script>