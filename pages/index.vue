<template>
  <div v-html="htmlContent"></div>
</template>

<script>
export default {
  async asyncData(context) {
    console.log(context)
    const htmlContent = await fetch('http://localhost:3000/script.txt').then((res) => res.text());
    return {
      htmlContent,
    };
  },
  data() {
    return {
      htmlContent: '',
    };
  },
  methods: {},
};
</script>

<style></style>
