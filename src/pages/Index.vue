<template>
  <Layout>

    <div class="container">

    <div class="text-center">
        <img src="https://i.ibb.co/VSFJdgr/notes-icon.png">
    </div>
      
    <g-link
      :to="item.node.path"
      v-for="item in $page.posts.edges"
      :key="item.node.id"
      class="blog-post">

      <div class="post">
          <h5 class="mt-0">{{item.node.title}}</h5>
      </div>

    </g-link>

    </div>


  </Layout>
</template>

<page-query>
query Blog {
  posts: allBlogPost(sortBy: "title", order: ASC) {
    edges {
      node {
        id
        path
        title
        excerpt
      }
    }
  }
}
</page-query>

<style lang="scss" scoped>

.media {
  img {
    width: 120px;
    height: 120px;
  }
}

.media-body {
  margin: auto;
}

a {
  color: #dddee0;
}

  a.post {
    text-decoration: none;
  }

  div.post {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    transition: 0.3s;
    padding: 2px 16px;
    margin: 24px;
  }
  div.post:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }


</style>

