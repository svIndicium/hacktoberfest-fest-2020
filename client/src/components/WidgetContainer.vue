<template>
  <div class="widget-container">
    <Example />
    <Crypto />
  </div>
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  components: {
    // ? Widgets here...
    Crypto: () => import("../../../modules/vue-cryptocurrency"),
    Example: () => import("../../../modules/vue-example"),
  },
});
</script>

<style lang="scss">
.widget-container {
  display: grid;
  grid-template-columns: repeat(4, minmax(360px, 1fr));
  grid-gap: 1.2rem;
  padding: 32px 24px 32px 24px;
  min-height: calc(100vh - 64px); // - nav height
  background: var(--secondary-background-color);

  .widget {
    background: var(--root-background-color);
    border-radius: 8px;
  }
}
</style>
