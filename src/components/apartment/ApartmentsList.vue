<template>
  <Container>
    <slot name="title"></slot>
    <div class="apartment-list">

      <template v-for="apartment in items">
        <slot name="apartment" v-bind:apartment="apartment"></slot>
      </template>
    </div>
    <slot name="description"></slot>
  </Container>
</template>

<script>
import Container from "@/components/shared/Container";

export default {
  name: "ApartmentsList",
  components: {
    Container
  },
  props: {
    items: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style lang="scss" scoped>
.apartment-list {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin: 0 auto;
}
</style>