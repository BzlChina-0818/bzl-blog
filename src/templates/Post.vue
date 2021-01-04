
<template>
  <Layout>
    <header class="masthead" 
        :style="{
          backgroundImage: `url(http://117.50.36.83:1337${ $page.post.cover[0].url})`
        }"
    >
      <div class="overlay"></div>
      <div class="container">
          <div class="row">
            <div class="col-lg-8 col-md-10 mx-auto">
              <div class="site-heading">
               <h1>{{ $page.post.title }}</h1>
              </div>
            </div>
          </div>
        </div>
      <div>
    
     
    </div>
    </header>
       <article>
      <div class="container">
        <div class="row">
           <div>{{ $page.post.content }}</div>
        </div> 
      </div>
    </article>
    
  </Layout>
</template>

<page-query>
query ($id: ID!) {
  post: strapiPost (id: $id) {
    id
    title
    content
    cover {
        url
    }
  }
}
</page-query>

<script>
export default {
  name: 'PostPage',
  metaInfo () {
    return {
      title: this.$page.post.title
    }
  }
  // metaInfo: {
  //   title: ''
  // }
}
</script>

<style>

</style>
