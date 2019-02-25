<template>
  <section class="single-recipe">
    <h1>{{ $route.params.id }}</h1>
    <div>
      <img :src="recipe.thumbnail" :alt="recipe.title" class="recipe-image">
    </div>
    <p>The recipe description</p>
    <p>{{ recipe.descriptionText }}</p>
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
              title: "Delicious Pizze",
              previewText: "Awesome Pizza!",
              descriptionText: "Wow",
              thumbnail:
                "https://cdn.cnn.com/cnnnext/dam/assets/171027052520-processed-foods-exlarge-tease.jpg"
            },
            {
              id: "2",
              title: "Delicous Fruits",
              previewText: "Awesome Fruit!",
              descriptionText: "Wow",
              thumbnail:
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdkWzRF2qil96cWUPUJj1k6kozcHiEJueetu1yh04XLKEKneE1"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1500);
    });
  }
};
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
