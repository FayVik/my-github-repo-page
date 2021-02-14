<template>
  <div class="navbar">
    <nav class="navbar-nav desktop-view">
      <div class="row col-4">
        <a href="#" class="logo">
          <font-awesome-icon :icon="['fab', 'github']" />
        </a>
        <input type="text" placeholder="Search or jump to..." />
        <ul class="nav-link">
          <li><a href="#" class="show">Pull requests</a></li>
          <li><a href="#" class="hide">Pull</a></li>
          <li><a href="#">Issues</a></li>
          <li><a href="#">Marketplace</a></li>
          <li><a href="#">Explore</a></li>
        </ul>
      </div>
      <div class="col-6">
        <a href="#">
          <font-awesome-icon :icon="['fa', 'bell']" />
        </a>
        <a href="#">
          <font-awesome-icon :icon="['fa', 'plus']" />
        </a>
        <a href="#">
          <font-awesome-icon :icon="['fa', 'user-circle']" />
        </a>
      </div>
    </nav>

    <nav class="mobile-view">
      <div class="views">
        <div class="menu col-3">
          <div>
            <button @click="menuButton()" class="social">
              <a href="#">
                <font-awesome-icon :icon="['fa', 'bars']" />
              </a>
            </button>
            <button @click="close()" class="social-2">
              <a href="#">
                <font-awesome-icon :icon="['fa', 'times']" id="social" />
              </a>
            </button>
          </div>
          <div class="mobile-menu">
            <input type="text" placeholder="Search or jump to..." />
            <ul class="">
              <li><a href="#">Pull requests</a></li>
              <li><a href="#">Issues</a></li>
              <li><a href="#">Marketplace</a></li>
              <li><a href="#">Explore</a></li>
            </ul>
          </div>
        </div>
        <div class="col-3 mobile-logo">
          <a href="#" class="logo">
            <font-awesome-icon :icon="['fab', 'github']" />
          </a>
        </div>
        <div class="col-3 mobile-bell">
          <a href="#">
            <font-awesome-icon :icon="['fa', 'bell']" />
          </a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  methods: {
    menuButton() {
      console.log("rrrr");
      const links = document.querySelector(".mobile-menu");
      const icon = document.querySelector(".social");
      const icon2 = document.querySelector(".social-2");
      let key = 1;
      if (key === 1) {
        key = 0;
        console.log(key);
        links.style.display = "block";
        icon.style.display = "none";
        icon2.style.display = "block";
      }
    },
    close() {
      const links = document.querySelector(".mobile-menu");
      const icon = document.querySelector(".social");
      const icon2 = document.querySelector(".social-2");
      let key = 1;
      if (key === 1) {
        key = 0;
        links.style.display = "none";
        icon.style.display = "block";
        icon2.style.display = "none";
      }
    }
  }
};
</script>

<style scoped>
.mobile-view {
  display: none;
}
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
  justify-content: start;
  align-items: center;
  min-height: 6vh;
}
.nav-link {
  min-width: 40%;
  display: flex;
  justify-content: start;
  align-items: center;
  min-height: 6vh;
}
ul li {
  list-style: none;
  padding-right: 20px;
}
ul li a {
  color: #fff;
  text-decoration: none;
}
ul li .hide {
  display: none;
}
.navbar-nav {
  display: flex;
  min-height: 6vh;
  width: 100%;
  justify-content: start;
  align-items: center;
}
.col-4 {
  width: 85%;
  padding: 0 0 0 20px;
}
.logo {
  color: #fff;
  font-size: 30px;
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
  padding-left: 8px;
  border-radius: 8px;
  border: 1px solid rgb(87, 87, 87);
}
.col-6 {
  width: 15%;
  text-align: center;
}
.col-6 a {
  margin-right: 15px;
  color: #fff;
  font-size: 20px;
}
.menu {
  padding: 5px 10px;
  font-weight: 800;
  display: none;
}

@media screen and (max-width: 834px) {
  ul li .hide {
    display: block;
  }
  .show {
    display: none;
  }
}

@media screen and (max-width: 745px) {
  .social-2 {
    display: none;
  }
  .desktop-view {
    display: none;
  }
  .views {
    display: flex;
    min-height: 10vh;
    justify-content: space-around;
    align-items: center;
    width: 100%;
  }
  .mobile-view {
    display: block;
  }
  .col-3 {
    width: 50%;
  }
  .menu {
    display: block;
    font-size: 28px;
  }
  .mobile-logo {
    text-align: center;
  }
  .mobile-bell {
    text-align: end;
    padding-right: 20px;
  }
  .mobile-bell a {
    color: #fff;
    font-size: 26px;
  }
  .mobile-menu {
    position: absolute;
    background: #161b22;
    left: 0%;
    top: 8%;
    right: 0;
    height: 40vh;
    padding: 26px 40px 0 26px;
    display: none;
  }
  .mobile-menu input {
    margin-bottom: 0;
    width: 100%;
    margin: 0;
  }
  ul {
    padding: 0;
  }
  ul li a {
    font-size: 14px;
  }
  ul li {
    padding: 0 20px 0 0;
    margin: 0;
    width: 100%;
    border-bottom: 3px solid;
  }
}
</style>
