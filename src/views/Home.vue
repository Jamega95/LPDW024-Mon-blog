<template>
  <div class="home-container">
    <h1 class="home-title">Bienvenue sur notre Blog</h1>
    <p class="home-description">Retrouvez ici nos derniers articles</p>
    <div v-for="article in articles" :key="article.id">
      <a :href="'#/article' + article.id" class="article-link">
        <article-card :article="article" />
      </a>
    </div>
  </div>
</template>

<script>
import ArticleCard from "@/components/ArticleCard.vue";

export default {
  components: {
    ArticleCard,
  },
  data() {
    return {
      articles: [
        {
          id: 1,
          title: "Titre de l'article 1",
          image: "image1.jpg",
          excerpt:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec justo non odio accumsan vehicula eu ac ligula. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posue cubilia Curae; Donec at arcu eu leo vehicula feugiat.",
        },
        {
          id: 2,
          title: "Titre de l'article 2",
          image: "image2.jpg",
          excerpt:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec justo non odio accumsan vehicula eu ac ligula. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posue cubilia Curae; Donec at arcu eu leo vehicula feugiat.",
        },
        {
          id: 3,
          title: "Titre de l'article 3",
          image: "image3.jpg",
          excerpt:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec justo non odio accumsan vehicula eu ac ligula. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posue cubilia Curae; Donec at arcu eu leo vehicula feugiat.",
        },
        {
          id: 4,
          title: "Titre de l'article 4",
          image: "image4.jpg",
          excerpt:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec justo non odio accumsan vehicula eu ac ligula. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posue cubilia Curae; Donec at arcu eu leo vehicula feugiat.",
        },
        {
          id: 5,
          title: "Titre de l'article 5",
          image: "image5.jpg",
          excerpt:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec justo non odio accumsan vehicula eu ac ligula. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posue cubilia Curae; Donec at arcu eu leo vehicula feugiat.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.home-container {
  text-align: center; /* Centrer le contenu horizontalement */
  padding: 20px;
}

.home-title {
  font-size: 24px;
  margin-bottom: 20px;
}

.home-description {
  font-size: 16px;
  margin-bottom: 20px;
}

/* Style pour les liens des articles */
.article-link {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  padding: 10px;
  gap: 10px;
  text-decoration: none; /* Supprimer la soulignement du texte des liens */
  color: #007bff; /* Couleur du texte bleu */
}

.articles-link > * {
  flex-basis: 33.33%;
  box-sizing: border-box;
  padding: 10px;
}

.article-link:hover {
  text-decoration: underline; /* Ajouter une soulignement au survol */
}
</style>
