<template>
  <section class="container">
    <div>
      <h1 class="title">sonicography</h1>
      <h2 class="subtitle">Studio Albums of Sonic Youth</h2>
      <div class="links">
        <a href="#" class="button-green">Confusion Is Sex</a>
        <a href="#" class="button-green">Bad Moon Rising</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
.title {
  display: block;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 60px;
  font-weight: bold;
  letter-spacing: 1px;
}
.subtitle {
  color: hsl(220, 20%, 50%);
  font-size: 42px;
  font-weight: 300;
  word-spacing: 5px;
}
.links {
  padding-top: 15px;
}
.button-green {
  display: inline-block;
  border: 1px solid hsl(170, 40%, 40%);
  border-radius: 4px;
  padding: 10px 30px;
  color: hsl(170, 40%, 40%);
  text-decoration: none;
}
.button-green:hover {
  color: #fff;
  background-color: hsl(170, 40%, 40%);
}
</style>
