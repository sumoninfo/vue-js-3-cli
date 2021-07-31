<template>
  <Suspense>
    <template #default>
      <div v-for="item in articleList" :key="item.id">
        <article>
          <h2>{{ item.title }}</h2>
          <p>{{ item.body }}</p>
        </article>
      </div>
    </template>
    <template #fallback>
      Articles loading...
    </template>
  </Suspense>
</template>

<script>
import axios from 'axios'

export default {
  name: "Article",
  async setup() {
    let articleList = await axios.get('https://jsonplaceholder.typicode.com/posts').then(response => {
      console.log(response.data)
      return response.data
    })
    return {
      articleList
    }
  }
}
</script>

<style scoped>

</style>
