<template>
  <nav class="nav">
    <div class="logo">
      <nuxt-link :to="{ name: 'index' }" class="logo text-lg"
        ><span class="sonic">sonic</span>ography</nuxt-link
      >
    </div>
    <div class="nav-content">
      <ul>
        <li class="nav-link">
          <nuxt-link :to="{ name: 'about' }">About</nuxt-link>
        </li>
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
  font-weight: bold;
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
.nav-link a {
  color: white;
  transition: all 0.3s ease;
}
.nav-link a:hover {
  color: var(--yellow);
}
</style>
