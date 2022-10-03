<template>
  <button class="base-button" type="submit">
    <slot></slot>
  </button>
</template>

<style scoped>
.base-button {
  margin-top: 25px;
  margin-bottom: 25px;
  display: flex;
  text-align: center;
  letter-spacing: 1px;
  font-size: 14px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  color: #37474f;
  font-weight: 500;
  line-height: 1em;
  padding: 0.5em 1em;
  width: max-content;
  justify-content: center;
  text-transform: uppercase;
  user-select: none;
  border-radius: 0.5em;
  border: 3px solid #ff8a80;
  background-color: white;
  transition: 0.25s all;
  cursor: pointer;
}

.base-button:hover {
  color: #62727b;
  border-color: #c85a54;
}
</style>