<template>
  <nav class="nav">
    <div class="logo">
      <nuxt-link :to="{ name: 'index' }" class="logo text-lg"
        >sonicography</nuxt-link
      >
    </div>
    <div class="nav-content">
      <ul>
        <li>About</li>
        <li>Band</li>
        <li>Info</li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 70px;
  font-weight: lighter;
  letter-spacing: 0.5px;
}
.nav .nav-content {
  font-size: 1rem;
}
.nav-content ul {
  display: flex;
  list-style: none;
}
.nav-content ul li {
  padding: 2px 10px;
}
.nav-content ul li:not(:first-of-type) {
  border-left: 1px solid rgba(255, 255, 255, 0.2);
}
</style>
