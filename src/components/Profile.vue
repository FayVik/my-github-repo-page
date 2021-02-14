<template>
  <div class="container">
    <div>
      <p class="img-container">
        <img src="../assets/fayviks.png" alt="Logo" />
      </p>
    </div>
    <div class="profile-content">
      <div class="profile-info">
        <h2>Favour vivian woka</h2>
        <span>FayVik </span>
        <p>I am a Full Stack Developer</p>
        <button>Edit Profile</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  /* text-align: center; */
}
.img-container {
  min-height: 30vh;
  margin-top: -15%;
}
img {
  width: 250px;
  border: 2px solid black;
  border-radius: 500px;
  height: 242px;
  padding: 10px;
}
span {
  font-size: 20px;
}
button {
  width: 80%;
  height: 5vh;
  border: 1px solid rgb(172, 171, 171);
  background: none;
  border-radius: 4px;
}
.profile-info {
  text-align: justify;
  padding-left: 88px;
}
</style>
