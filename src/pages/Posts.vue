<template>
  <div>
    <h2>All Posts</h2>
    <div v-for="edge in $page.posts.edges" :key="edge.node.id">
      <h2>{{ edge.node.id }}</h2>
    </div>
  </div>
</template>

<page-query>
query {
  posts: allPost {
    edges {
      node {
        id
      }
    }
  }
}
</page-query>

<script>
export default {};
</script>

<style></style>
