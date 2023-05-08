<script setup lang="ts">
import { ref } from 'vue';

const items2 = ref<any[]>([1]);
const items = ref<any[]>([1]);
</script>

<template>
<div class="container">
<div class="top">
  <button @click="items2.push(1)">add</button>
  <div class="list">
      <div v-for="item in items2" class="item">
          <p>あああ</p>
          <div class="body">
              <p>いいい</p>
              <div class="inner">
                  <div class="inner1">
                    <div class="inner2">
                      <img src="https://files-p1.a9z.dev/p1/7bfb8df3-692b-487b-9b34-2fb3fd21a3a0.jpg" height="100" width="10" class="img" />
                    </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</div>
<div class="top">
  <button @click="items.push(1)">add</button>
  <div class="list">
      <div v-for="item in items" class="item">
          <p>あああ</p>
          <div class="body">
              <p>いいい</p>
              <div class="inner">
                  <div class="inner1">
                    <div class="inner2">
                      <img height="100" width="10" class="img" />
                    </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</div>
</div>
</template>

<style scoped>
.container {
  height: 100vh;
  display: flex;
  flex-direction: column;
}
.top {
    width: 100%;
    height: 100%;
    overflow-y: auto;
    padding: 1em;
    background-color: #000;
    color: #fff;
    container-type: size;
}
.list {
    background-color: #fff;
    color: #000;
}
.item {
    padding: 1em;
    background-color: #000;
    color: #fff;
}
.body {
    height: 300px;
    background-color: #0ff;
    color: #000;
    container-type: inline-size;
}
.inner {
    background-color: #f00;
}
.inner1 {
	min-height: 64px;
	max-height: clamp(
		64px,
		50cqh,
		min(360px, 50vh)
	);
  overflow: clip;
}
.inner2 {
	position: relative;
	width: 100%;
	height: 100%;
}
.img {
	display: block;
	width: 100%;
	height: 100%;
}
</style>
