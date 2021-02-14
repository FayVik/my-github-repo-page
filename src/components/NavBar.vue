<template>
  <div class="navbar">
    <nav class="navbar-nav">
      <div class="row col-4">
        <img src="" alt="Logo" />
        <input type="text" placeholder="Search or jump to..." />
        <ul class="nav-link">
          <li><a href="">Pull requests</a></li>
          <li><a href="">Issues</a></li>
          <li><a href="">Marketplace</a></li>
          <li><a href="">Explore</a></li>
        </ul>
      </div>
      <div class="col-6"></div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style scoped>
.navbar {
  min-height: 6vh;
  width: 100%;
  background: #161b22;
  color: #fff;
  margin: 0;
  padding: 0;
}
.row {
  display: flex;
  justify-content: space-around;
  align-items: center;
  min-height: 6vh;
}
.nav-link {
  min-width: 40%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  min-height: 6vh;
}
ul li {
  list-style: none;
}
ul li a {
  color: #fff;
  text-decoration: none;
}
.navbar-nav {
  display: flex;
  min-height: 6vh;
  width: 100%;
}
.col-4 {
  width: 80%;
  background-color: blueviolet;
  padding: 0 10px 0 20px;
}
input {
  width: 30%;
  margin-left: 20px;
  border: 1px solid;
  background-color: #0d1117;
  height: 5vh;
  outline: none;
  box-shadow: none;
  color: #b3bcbd;
}
</style>
