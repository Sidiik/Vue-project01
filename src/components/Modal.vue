<template>
  <div class="backdrop" ref="backdrop">
    <div class="modal" ref="modal">
      <h1>{{ header }}</h1>
      <p>Modal content here</p>
      <button @click="handleClick">close</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["header"],
  methods: {
    handleClick() {
      this.$refs.modal.classList.add("hide");
      this.$refs.backdrop.classList.add("hide");
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
.backdrop .hide {
  display: none;
}
.modal {
  background-color: white;
  width: 50%;
  margin: auto;
  padding: 2rem;
  border-radius: 0.4rem;
  transform-origin: top;
  transition: all 0.3s ease;
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
.hide {
  opacity: 0;
  transform: scale(1, 0);
}
</style>
