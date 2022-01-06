<template>
  <div class="place">
    <img :src="image" width="235" height="300" />
    <h2>{{ name }}</h2>
    <p>{{ description }}</p>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "CityCard",
  props: {
    name: String,
    image: String,
    description: String,
  },
};
</script>