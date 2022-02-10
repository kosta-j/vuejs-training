<template>
  <div :id="$style.app">
    <ApartmentsList :items="apartments">
      <template v-slot:title>Title</template>
      <template v-slot:apartment="{apartment}">
        <ApartmentItem
            :key="apartment.id"
            :descr="apartment.descr"
            :rating="apartment.rating"
            :price="apartment.price"
            :imgSrc="apartment.imgUrl"
        />
      </template>

      <template v-slot:description>Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aperiam blanditiis
        facilis laboriosam porro repellendus! Architecto consequuntur fugit illum incidunt, minima nesciunt numquam
        obcaecati officia optio quis sed temporibus vel!
      </template>
    </ApartmentsList>
  </div>
</template>

<script>
import ApartmentsList from "@/components/apartment/ApartmentsList";
import ApartmentItem from "@/components/apartment/ApartmentItem";
import apartments from "@/components/apartment/apartments";

export default {
  name: "App",
  components: {
    ApartmentsList,
    ApartmentItem
  },
  data() {
    return {
      apartments,
    }
  }
}
</script>

<style module>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
