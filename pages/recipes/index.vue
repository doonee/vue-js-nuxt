<template>
  <section class="recipes">
    <Recipe 
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail" 
      :title="recipe.title" 
      :previewText="recipe.previewText"
      :id="recipe.id" />
  </section>
</template>

<script>
import Recipe from '../../components/recipes/Recipe'
export default {
  components: {
    Recipe
  },
  asyncData() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "awesome pizza",
              previewText: "very delicious dorami pizza!!",
              thumbnail: "http://www.newmarketpizza.com/upload/5.jpg"
            },
            {
              id: "2",
              title: "wellbeing salad",
              previewText: "for your health! eat salad everyday!!",
              thumbnail: "https://hips.hearstapps.com/del.h-cdn.co/assets/16/21/1464036871-delish-summer-salads-chicken-fajita.jpg"
            }
          ]
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
</style>
