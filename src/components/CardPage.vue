<template>
  <div>
    <div class="container">
      <div class="container-content" v-for="datas in data" :key="datas.id">
        <div class="container-text">
          <h2>
            <a :href="datas.html_url"> {{ datas.name }} </a>
          </h2>
          <span class="languages">{{ datas.language }} </span>
          <span> {{ moment(datas.updated_at).fromNow() }}</span>
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
export default {
  name: "CardPage",
  data() {
    return {
      data: ""
    };
  },
  mounted() {
    this.getRepo();
  },
  methods: {
    async getRepo() {
      try {
        const response = await fetch(
          "https://api.github.com/users/FayVik/repos"
        );
        const data = await response.json();
        this.data = data;
        console.log(this.data);
      } catch (error) {
        console.error(error);
      }
    }
  }
};
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
