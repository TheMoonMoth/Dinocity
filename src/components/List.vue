<template>
  <main>
    <h2>Job Listings</h2>
    <ul>
        <li v-for="job in this.props.listings" :key="job.id">{{job}}</li>
    </ul>
  </main>
</template>

<script>
export default {
  name: "List"
};
</script>

<style>

</style>
