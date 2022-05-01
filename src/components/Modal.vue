<template>
  <div :class="{ modal: theme === 'sale' }">
    <slot />
    <p>The Modal</p>
    <div class="actions">
        <!-- When we want a dynamic slot   -->
      <slot name="links" />
    </div>
  </div>
</template>

// props 

<script>
export default {
  name: "Modal",
  props: ["theme"],
  data() {},
};
</script>

<style scoped>
h1 {
  color: pink;
}

.modal {
  background: crimson;
  width: 300px;
  justify-content: center;
  display: flex;
  align-items: center;
  color: #fff;
}
</style>