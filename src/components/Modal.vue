<template>
  <div class="backdrop">
    <div class="modal">
      <h1>Modal title</h1>
      <p>Modal content here</p>
      <button>close</button>
    </div>
  </div>
</template>

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
}
.modal {
  background-color: white;
  width: 50%;
  margin: auto;
  padding: 2rem;
  border-radius: 0.4rem;
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
</style>
