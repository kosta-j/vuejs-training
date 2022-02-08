<template>
  <h1>{{ titleText }}</h1>
</template>
<script>
export default {
  name: "Title",
  props: {
    titleText: String,
  },
};
</script>
