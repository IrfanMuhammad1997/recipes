<template>
    <section class="recipes">
        <Recipe
          thumbnail="https://assets3.thrillist.com/v1/image/2797371/size/tmg-article_default_mobile.jpg"
          title="Burger Lezat"
          priviewText="Sangat lezat!"
          id="1"
        />

        <Recipe
          thumbnail="https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/veggie_paella_29921_16x9.jpg"
          title="Nasi Kuning"
          priviewText="Mantap jiwa!"
          id="2"
        />
    </section>
</template>

<script>
  import Recipe from "@/components/Recipe"

  export default {
      components: {
          Recipe
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
