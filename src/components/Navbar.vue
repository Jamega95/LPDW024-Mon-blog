<template>
  <div class="navbar">
    <a href="#/">Home</a> | <a href="#/article1">Article 1</a> |
    <a href="#/article2">Article 2</a> | <a href="#/article3">Article 3</a> |
    <a href="#/article4">Article 4</a> | <a href="#/article5">Article 5</a> |
    <a href="#/not-found">Broken link</a>
  </div>
</template>

<style scoped>
.navbar {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 1000px;
  margin-left: 440px;
  gap: 2%;
  padding: 10px;
  background-color:  #f0f0f0;
;
  border-radius: 20px;
}
</style>
