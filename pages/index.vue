<template>
  <div v-html="htmlContent"></div>
</template>

<script>
export default {
  async asyncData() {
    const htmlContent = await fetch(
      'https://githubrhmnjf-adkb--3000--70dbe416.local-credentialless.webcontainer.io/script.txt'
    ).then((res) => res.text());
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
