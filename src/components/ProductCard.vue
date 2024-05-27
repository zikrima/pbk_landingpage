<!-- src/components/ProductCard.vue -->
<template>
  <q-card class="my-card" bordered>
    <q-img :src="image" :alt="title" height="140px" />
    <q-card-section>
      <div class="text-h6">{{ title }}</div>
      <div>{{ description }}</div>
    </q-card-section>
    <q-card-actions align="right">
      <q-btn flat label="View" color="primary" />
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
    image: String
  }
}
</script>

<style>
.my-card {
  width: 300px;
}
</style>
