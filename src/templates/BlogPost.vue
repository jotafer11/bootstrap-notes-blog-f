<template>
  <Layout>
    <div class="container">

    <div class="blogPost">
      <h1 v-html="$page.post.title" class="text-center mb-4"/>
      <BlogContent class="mt-5" :content="$page.post.content"/>
    </div>      
      
    </div>

  </Layout>
</template>

<page-query>
query BlogPost ($path: String!) {
  post: blogPost (path: $path) {
    title
    content
  }
}
</page-query>

<script>
import BlogContent from '@/components/BlogContent'

export default {
  components: {
    BlogContent,
  },
  metaInfo() {
    return {
      title: this.$page.post.title,
    }
  },
}
</script>

<style lang="scss" scoped>


.meta {
  display: flex;
}

.box {
  display: flex;
  flex-direction: column;
  padding: 0 20px 0 0;
  
  .label {
    font-weight: bold;
  }
}

</style>
