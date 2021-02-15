<template>
  <div class="containers">
    <p>© 2021 GitHub, Inc.</p>
    <p><a href="#">Terms </a></p>
    <p><a href="#">Privacy </a></p>
    <p><a href="#">Security </a></p>
    <p><a href="#">Status </a></p>
    <p><a href="#">Docs </a></p>
    <div class="logo">
      <a href="#" class="">
        <font-awesome-icon :icon="['fab', 'github']" />
      </a>
    </div>
    <p><a href="#">Contact </a></p>
    <p><a href="#">GitHub </a></p>
    <p><a href="#">Pricing </a></p>
    <p><a href="#">API </a></p>
    <p><a href="#">Training </a></p>
    <p><a href="#">Blog </a></p>
    <p><a href="#">About </a></p>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.containers {
  width: 99%;
  min-height: 16vh;
  color: rgb(75, 75, 75);
  display: flex;
  justify-content: space-around;
  align-items: center;
  font-size: 12px;
}
p {
  margin-right: 26px;
}
a {
  text-decoration: none;
  color: rgb(0, 119, 255);
  font-size: 12px;
}
a:hover {
  border-bottom: 1px solid blue;
}
.logo {
  width: 10%;
  text-align: center;
}
.logo a {
  font-size: 20px;
  color: rgb(109, 109, 109);
}
.logo a:hover {
  color: rgb(75, 75, 75);
}
</style>
