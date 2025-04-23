<script setup></script>

<template>
  <footer>
    <p>
      Made with <span>Vue.js </span>by
      <a href="https://github.com/Christelle-Labin" target="_blank"
        ><span>Labin Christelle</span></a
      >
    </p>
  </footer>
</template>

<style scoped>
footer {
  border-top: 1px solid var(--main-yellow);
  display: flex;
  justify-content: center;
  align-items: center;
  height: var(--footer-height);
}
a {
  text-decoration: none;
  font-weight: bold;
  color: var(--main-yellow);
}
</style>
