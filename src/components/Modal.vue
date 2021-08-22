<template>
  <div class="backdrop" ref="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <slot></slot>
      <div class="actions">
        <slot name="links"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["header", "text", "theme"],
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<style scoped>
.backdrop {
  top: 0;
  position: fixed;
  background-color: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  height: 100vh;
  transition: all 0.3s ease;
}

.modal {
  background-color: white;
  width: 30%;
  margin: auto;
  padding: 3rem;
  border-radius: 0.4rem;
  transform-origin: top;
  transition: all 0.3s ease;
}

.actions {
  margin-top: 2rem;
}

h1 {
  color: red;
}
button {
  background: blue;
  color: white;
  padding: 0.3rem 1rem;
  border: 0;
  outline: 0;
  border-radius: 0.2rem;
  cursor: pointer;
  font-size: 1rem;
}
.modal.sale {
  background: crimson;
  color: white;
}
.modal.sale h1 {
  color: white;
}
</style>
