<script lang="ts">
import { computed, defineComponent } from "vue";
import { useRoute } from "vue-router";

export default defineComponent({
  name: "TheAppLayout",
  setup() {
    const route = useRoute();
    const layout = computed(() => {
      const layout = route?.meta?.layout;
      if (layout) {
        return layout;
      }
      return "div";
    });
    return {
      layout,
    };
  },
});
</script>

<template>
  <component :is="layout">
    <router-view />
  </component>
</template>
