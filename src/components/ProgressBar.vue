<template>
  <div class="progress">
    <div class="progress__inner">
      <span>0%</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProgressBar",
};
</script>

<style>
.progress {
  width: 100%;
  height: 20px;
  background: #fff;
  position: relative;
}
.progress__inner {
  height: 100%;
  background: linear-gradient(to right, gold, red, black);
  border-radius: 0 10px 10px 0;
}
.progress__inner.full {
  border-radius: 0;
}
.progress__inner span {
  color: #fff;

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
