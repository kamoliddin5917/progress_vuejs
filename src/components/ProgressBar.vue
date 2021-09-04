<template>
  <div class="progress">
    <div
      :class="progress == 100 ? 'progress__inner full' : 'progress__inner'"
      :style="`width:${progress}%`"
    >
      <span :class="progress > 50 ? 'white' : ''">{{ progress }}%</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProgressBar",
  props: ["progress"],
};
</script>

<style>
.progress {
  width: 100%;
  height: 20px;
  background: gold;
  box-shadow: 0 2px 4px #000;
  position: relative;
}
.progress__inner {
  height: 100%;
  background: linear-gradient(to right, gold, orange, red, #333, black);
  border-radius: 0 10px 10px 0;
}
.progress__inner.full {
  border-radius: 0;
}
.progress__inner span {
  color: red;

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.progress__inner .white {
  color: #fff;
}
</style>
