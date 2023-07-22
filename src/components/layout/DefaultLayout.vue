<template>
  <div class="wrapper flex-center h-100 main-purple">
    <CardItem class="mr-5"/>
    <CardItem class="mr-5" />
    <CardItem class="mr-5" />
    <CardItem class="mr-5" />
  </div>
</template>

<script lang="ts">
import { defineAsyncComponent, defineComponent, ref } from "vue";

export default defineComponent({
  name: "DefaultLayout",
  components: {
    CardItem: defineAsyncComponent(
      () => import("@/components/CardItem.vue")
    ),
  },
});
</script>

<style scoped lang="scss">
.wrapper-block {
  max-width: 320px;
  width: 100%;
  border-radius: 20px;

  img {
    width: 24px;
  }
}
.card {
  &-top {
    background-image: url("/src/assets/img/figure-1.svg");
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    min-height: 65px;
  }
  &-content {
    border-radius: 20px;
    padding: 20px;
    border-width: 3px;
  }
  &-bottom {
    background-image: url("/src/assets/img/figure-2.svg");
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    min-height: 65px;
  }
}
</style>
