<template>
  <header>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/recipes">Recipe</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/_samples/gridExample">gridExample</nuxt-link>
        </li>
        <li>
          <a target="_blnak" href="http://doonee.net">about doonee</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style scoped>
header {
  width: 100%;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color:#521751;
}
ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
li {
  margin: 0 10px;
}
a{
  text-decoration: none;
  color:#fff;
}
</style>
