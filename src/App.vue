<template>
  <div id="app">
    <main>
      <div class="navigation">
        <header>
          <h1>Kamoliddin Jamoliddinov</h1>
        </header>
        <nav>
          <a href="#">About us</a>
          <a href="#">Contact</a>
          <a href="#">Portfolio</a>
        </nav>
      </div>
      <ProgressBar :progress="progress" />
      <Post @progressUpdate="setProgress" />
    </main>
  </div>
</template>

<script>
import Post from "./components/Post";
import ProgressBar from "./components/ProgressBar";

export default {
  name: "App",
  components: {
    Post,
    ProgressBar,
  },
  data() {
    return { progress: 0 };
  },
  methods: {
    setProgress(progress) {
      this.progress = progress;
    },
  },
};
</script>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  scroll-behavior: smooth;
}
body {
  font-family: "monserrat", sans-serif;
}
main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  overflow: hidden;
  background: gold;
}

.navigation {
  visibility: 100%;
  height: 10vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #000;
  padding: 30px;
}
header h1 {
  color: #fff;
  font-size: 32px;
}
a {
  display: inline-block;
  text-decoration: none;
  color: tomato;
  font-size: 16px;
  font-weight: 600;
  letter-spacing: 2px;
  padding: 5px 10px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  transition: all 0.4s;
}
a:hover {
  color: #fff;
  border-top: 1px solid tomato;
  border-bottom: 1px solid tomato;
}
</style>
