<template>
  <q-page>
    <CarouselItem></CarouselItem>
    <SliderItem></SliderItem>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import SliderItem from "src/components/SliderItem.vue";
import CarouselItem from "components/CarouselItem.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    SliderItem,
    CarouselItem,
  },
});
</script>
