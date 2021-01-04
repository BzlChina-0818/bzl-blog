<template>
  <!-- <div></div> -->
   <Layout>
      <header class="masthead" style="background-image: url('img/home-bg.jpg')">
        <div class="overlay"></div>
        <div class="container">
          <div class="row">
            <div class="col-lg-8 col-md-10 mx-auto">
              <div class="site-heading">
                <h1>Clean Blog</h1>
                <span class="subheading">A Blog Theme by Start Bootstrap</span>
              </div>
            </div>
          </div>
        </div>
      </header>

        <!-- <slot /> -->

      <div class="container">
        <div class="row">
          <div class="col-lg-8 col-md-10 mx-auto">
            <div class="post-preview" v-for="edge in $page.posts.edges" :key="edge.node.id">
              <g-link :to="/post/ + edge.node.id">
                <p class="post-meta"> {{edge.node.title}} </p>
              </g-link>
            
                <p class="post-meta"> {{edge.node.content}} </p>
            </div>
            <!-- <div class="clearfix">
              <a class="btn btn-primary float-right" href="#">Older Posts &rarr;</a>
            </div> -->
          </div>
        </div>
      </div>
   </Layout>
</template>
<page-query>
query {
  posts: allStrapiPost {
    edges {
      node {
        id
        title
      	content
        cover {
          url
        }
      }
    }
  }
}
</page-query>
