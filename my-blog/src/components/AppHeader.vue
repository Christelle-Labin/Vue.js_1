<script setup></script>

<template>
  <header>
    <div class="container">
      <img src="/src/assets/pictures/my-blog-avatar_xhjc4e.png" alt="pingouin" />
      <h2>My blog</h2>
    </div>
  </header>
</template>

<style scoped>
header {
  height: var(--header-height);
  border-bottom: 1px solid var(--main-yellow);
  padding: 10px 0;
}
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
}
img {
  height: 100%;
}
</style>
