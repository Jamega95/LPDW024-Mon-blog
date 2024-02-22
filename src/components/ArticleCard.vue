<template>
  <div class="article-card">
    <a :href="'#/article' + article.id">
      <img :src="article.image" alt="Image de l'article" />
      <h2>{{ article.title }}</h2>
      <p>{{ article.excerpt }}</p>
    </a>
  </div>
</template>

<script>
export default {
  props: ["article"],
};
</script>

<style scoped>
.article-card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center; /* Centrer verticalement les cartes */
  min-height: 100vh; /* Garantir que la section occupe au moins la hauteur de l'écran */
}

.article-card {
  border: 1px solid #ccc;
  margin: 10px;
  padding: 10px;
  max-width: 1000px;
  flex: 0 0 calc(50% - 20px); /* Afficher 2 cartes par ligne (50% de la largeur) */
}

/* Styling pour le dernier article */
.last-article {
  flex: 0 0 calc(100% - 20px); /* Afficher le dernier article en pleine largeur */
}

.article-card img {
  max-width: 100%;
}

.article-card h2 {
  font-size: 18px;
  margin: 10px 0;
}

.article-card p {
  font-size: 14px;
}

.article-card a {
  display: block;
  text-align: right;
  color: #007bff;
  text-align: center;
}
</style>
