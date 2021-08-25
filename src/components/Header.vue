<template>
  <h1 class="heading" :class="{ 'bg-red': theme === 'contact' }">
    {{ title }}
  </h1>
  <p>{{ content }}</p>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: "",
      required: true,
    },
    content: {
      type: String,
      default: "",
      required: true,
    },
    theme: {
      default: "",
      validator(value) {
        return ["example", "sales", "contact"].includes(value);
      },
    },
  },
};
</script>
<style scoped>
.heading {
  font-size: 30px;
}
.bg-red {
  background-color: red;
}
</style>
