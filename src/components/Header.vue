<template>
  <header>
      <img src="../assets/g-dino.png" alt="G Dino Logo" />
      <button @click="increment">Add one</button>
      <p>{{count}}</p>
  </header>
</template>

<script>
import Store from "../vuex/store"

export default {
    name: 'Header',
}
</script>

<style>
header img {
    height: 100px;
    width: auto;
}
</style>
