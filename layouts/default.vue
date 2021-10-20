<template>
  <div>
    <TheNavbar />
    <Nuxt />
  </div>
</template>

<script>
import TheNavbar from "@/components/TheNavbar";
export default {
  components: {
    TheNavbar
  }
};
</script>

<style>
.button-green {
  display: inline-block;
  vertical-align: text-top;
  max-width: 260px;
  border: 1px solid hsl(170, 40%, 40%);
  border-radius: 4px;
  margin: 5px;
  padding: 10px 30px;
  color: hsl(170, 40%, 40%);
  text-decoration: none;
}
.button-green:hover {
  color: #fff;
  background-color: hsl(170, 40%, 40%);
}
.button-green:hover img {
  opacity: 0.5;
}
</style>
