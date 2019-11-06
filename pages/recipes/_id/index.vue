<template>
  <section class="single-recipe">
    <h1>{{ recipes.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipes.thumbnail" :alt="recipes.title">
    </div>
    <p>{{ recipes.descriptionText }}</p>
    <nuxt-link to="/recipes">Back to recipes</nuxt-link>
  </section>
</template>

<script>
  export default {
      asyncData(context) {
          return new Promise((resolve, reject) => {
              setTimeout(() => {
                  resolve({
                      recipes: [
                          {
                              id: "1",
                              title: "Burger Lezat",
                              priviewText: "Sangat lezat!",
                              descriptionText: "Sangat enak dan mantap, wajib dicoba!",
                              thumbnail: "https://assets3.thrillist.com/v1/image/2797371/size/tmg-article_default_mobile.jpg"
                          },
                          {
                              id: "2",
                              title: "Nasi Kuning",
                              descriptionText: "Sangat enak dan mantap, wajib dicoba!",
                              thumbnail: "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/veggie_paella_29921_16x9.jpg"
                          }
                      ].find(el => el.id === context.params.id)
                  })
              }, 1500)
          })
      }
  }
</script>

<style scoped>
  .single-recipe {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
  }

  .recipe-image {
    width: 100%;
  }
</style>
