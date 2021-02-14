<template>
  <div>
    <div class="container">
      <div class="container-content">
        <div class="container-text">
          <h2>
            <a href="#">
              my-github-repo-page
            </a>
          </h2>
          <span>Vue </span> <span> Updated 4 hours ago </span>
        </div>
        <div class="container-button">
          <p>
            <button>
              Star
            </button>
          </p>

          <span>__________________</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  min-height: 18vh;
  width: 99%;
}
.container-content {
  border-bottom: 1px solid rgb(219, 219, 219);
  min-height: 18vh;
  display: flex;
  align-content: center;
  justify-content: flex-start;
}
.container-text {
  padding-left: 20px;
  width: 70%;
}
a {
  font-size: 18px;
  color: rgb(0, 60, 255);
  text-decoration: none;
}
.container-text span {
  font-size: 14px;
  color: rgb(119, 119, 119);
  margin-right: 20px;
}
.container-button {
  text-align: end;
  width: 30%;
  padding-right: 5px;
}
button {
  height: 5vh;
  border: 1px solid rgb(226, 226, 226);
  width: 26%;
  border-radius: 8px;
}
p {
  margin-bottom: 0;
}
.container-button span {
  color: green;
}
h2 {
  margin-bottom: 6px;
}
</style>
