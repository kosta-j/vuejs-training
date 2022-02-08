<template>
  <Container>
    <div class="apartment-list">
      <ApartmentItem
          v-for="{id, descr, rating, price, imgUrl} in items"
          :key="id"
          :descr="descr"
          :rating="rating"
          :price="price"
          :imgSrc="imgUrl"
          class="apartment-list__item"
      />
    </div>
  </Container>
</template>

<script>
import ApartmentItem from "@/components/apartment/ApartmentItem";
import Container from "@/components/shared/Container";

export default {
  name: "ApartmentsList",
  components: {
    ApartmentItem,
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

  &__item {
    margin-bottom: 30px;
  }
}
</style>