<template>
  <div class="">
    <NavBar />
    <div class="container">
      <div class="nav-pill">
        <ul>
          <li><a href="#">Overview</a></li>
          <li class="active"><a href="#">Repositories</a></li>
          <li><a href="#">Project</a></li>
          <li><a href="#">Package</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "./NavBar";
export default {
  name: "HelloWorld",
  props: {},
  components: {
    NavBar
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 100%;
  height: 88.5vh;
}
.nav-pill {
  height: 12vh;
  border-bottom: 2px solid black;
}
ul {
  display: flex;
  margin: 0;
  padding: 0;
  justify-content: center;
  align-items: flex-end;
  height: 12vh;
  width: 100%;
}
ul li {
  padding: 0 24px 8px 24px;
  list-style: none;
}
ul li a {
  text-decoration: none;
  font-size: 18px;
  color: rgb(68, 68, 68);
}
.active {
  color: black;
  border-bottom: 2px solid orangered;
}
</style>
