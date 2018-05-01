<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img :src="recipe.thumbnail" :alt="recipe.title" class="recipe-image">
    </div>
    <p>{{ recipe.previewText }}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
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
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.single-recipe{
  display: flex;
  flex-flow:column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
.recipe-image{
  width:100%;
}
</style>
