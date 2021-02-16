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
      <div class="container-content">
        <div class="left-side">
          <Profile />
        </div>
        <div class="right-side">
          <div class="top-right">
            <div class="right-input">
              <input type="text" placeholder="Find a repositories" />
            </div>
            <div class="top-left">
              <button class="select1">
                <select name="" id="">
                  <option value="">Type: All</option>
                </select>
              </button>
              <button class="select1">
                <select name="" id="">
                  <option value="">Language: All</option>
                </select>
              </button>
              <button type="button" class="btn">New</button>
            </div>
          </div>
          <div class="">
            <CardPage />
          </div>
        </div>
      </div>
      <div class="preview">
        <button><a href="#">Pervious </a></button>
        <button><a href="#">Next </a></button>
      </div>
    </div>
    <FooterPage />
  </div>
</template>

<script>
import NavBar from "./NavBar";
import CardPage from "./CardPage";
import Profile from "./Profile";
import FooterPage from "./FooterPage";
export default {
  name: "HelloWorld",
  props: {},
  components: {
    NavBar,
    CardPage,
    Profile,
    FooterPage
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 100%;
  min-height: 88.5vh;
}
.nav-pill {
  height: 16vh;
  border-bottom: 1px solid rgb(211, 211, 211);
}
ul {
  display: flex;
  margin: 0;
  padding: 0;
  justify-content: center;
  align-items: flex-end;
  height: 16vh;
  width: 100%;
}
ul li {
  padding: 0 24px 8px 24px;
  list-style: none;
}
ul li a {
  text-decoration: none;
  font-size: 14px;
  color: rgb(46, 46, 46);
}
.active {
  border-bottom: 2px solid rgb(243, 93, 39);
}
.active a {
  color: black;
  font-weight: 600;
}
.container-content {
  display: flex;
  justify-content: start;
  min-height: 72.3vh;
}
.left-side {
  width: 30%;
  height: 72.3vh;
  text-align: center;
}
.right-side {
  width: 66%;
}
.top-right {
  height: 10vh;
  display: flex;
  justify-content: start;
  align-items: center;
  width: 99%;
  border-bottom: 1px solid rgb(212, 212, 212);
}
.top-left {
  display: flex;
  align-items: center;
  height: 10vh;
  justify-content: start;
  padding-right: 5px;
}
.top-left .btn {
  background: green;
  height: 5vh;
  padding: 0 20px;
  border: none;
  border-radius: 4px;
  color: #fff;
  cursor: pointer;
}
.top-left select {
  height: 5vh;
  border-radius: 8px;
  background: none;
  border: none;
  outline: none;
}
.select1 {
  height: 5vh;
  background: none;
  border: 1px solid rgb(185, 185, 185);
  padding: 0 20px;
  border-radius: 4px;
  margin-right: 10px;
}
.right-input {
  width: 60%;
  display: flex;
  align-items: center;
  height: 10vh;
  justify-content: center;
  align-self: center;
}
input {
  height: 5vh;
  width: 90%;
  border-radius: 8px;
  border: 1px solid rgb(185, 185, 185);
  outline: none;
  padding-left: 6px;
}
button {
  outline: none;
}
.preview {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 18vh;
  border-bottom: 1px solid rgb(204, 204, 204);
}
.preview button {
  background: none;
  padding: 8px 18px;
  border-radius: 4px;
  border: 1px solid rgb(185, 185, 185);
}
.preview button a {
  color: rgb(0, 132, 255);
  text-decoration: none;
}
</style>
