<template>
  <div class="article">
    <h1>{{ article.title }}</h1>
    <img :src="article.image" alt="Image de l'article" />
    <p>{{ article.content }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      article: {
        title: "Lorem ipsum dolor",
        image: "image5.jpg",
        content: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed
          nec justo non odio accumsan vehicula eu ac ligula. Vestibulum
          ante ipsum primis in faucibus orci luctus et ultrices posuere
          cubilia Curae; Donec at arcu eu leo vehicula feugiat. Nulla
          facilisi. Cras quis laoreet velit. Duis at enim a eros vehicula
          iaculis nec nec eros. Sed at ligula at elit interdum lacinia in
          non urna. Sed porta vestibulum malesuada. Proin in efficitur
          augue. In a metus vel odio dapibus volutpat. Phasellus
          ullamcorper, arcu in luctus sodales, ex orci luctus nisi, vel
          suscipit eros odio at velit. Vestibulum nec nulla quis libero
          sollicitudin venenatis. Sed tristique turpis vel ante lacinia,
          sit amet dictum libero blandit. Nam sit amet lorem eget neque
          varius ultricies et et ex.`,
      },
    };
  },
};
</script>

<style scoped>
.article {
  padding: 20px;
}

.article h1 {
  font-size: 24px;
  margin-bottom: 10px;
}

.article img {
  max-width: 100%;
  margin-bottom: 10px;
}

.article p {
  font-size: 16px;
  line-height: 1.6;
}
</style>
