<template>
  <header>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Starting Page</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/recipes">Recipes</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">About</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  width: 100%;
  height: 30px;
  display: flex;
  justify-content: center;
  align-content: center;
  background-color: aquamarine;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-content: center;
}

li {
  margin: 0 10px;
}

a {
  text-decoration: none;
}
</style>
