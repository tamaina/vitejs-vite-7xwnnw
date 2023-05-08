<script setup lang="ts">
import { ref } from 'vue';

const items2 = ref<any[]>([1]);
const items = ref<any[]>([1]);
const windows = ref<any[]>([1]);
</script>

<template>
  <div class="container">
    <div class="c1">
      <button class="button" @click="items2.unshift(1)">add</button>
      <div class="list">
        <div v-for="(item, i) in items2" :key="i" class="item">
          <p>header</p>
          <div class="body">
            <p>body</p>
            <div class="inner">
              <div class="inner1">
                <div class="inner2">
                  <img src="./assets/vue.svg" class="img" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="c2">
      <button class="button" @click="items.unshift(1)">add</button>
      <div class="list">
        <div v-for="(item, i) in items" :key="i" class="item">
          <p>header</p>
          <div class="body">
            <p>body</p>
            <div class="inner">
              <div class="inner1">
                <div class="inner2">
                  <img src="./assets/vue.svg" class="img" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="c3">
      <button @click="windows.push(1)">add window</button>
    </div>
    <div v-for="window in windows" class="window">
      <div style="height: 50cqh; background: #00f">ええ</div>
    </div>
  </div>
</template>

<style scoped>
.container {
  height: 100vh;
  display: flex;
  flex-direction: row;
  overflow-x: auto;
}
.c1 {
  width: 330px;
  min-width: 330px;
  height: 100%;
  background-color: #000;
  color: #fff;
}
.c2 {
  width: 330px;
  min-width: 330px;
  height: 50%;
  background-color: #000;
  color: #fff;
}
.button {
  height: 50px;
}
.list {
  height: calc(100% - 50px);
  background-color: #f0f;
  color: #000;
  overflow-y: auto;
  container-type: size;
}
.item {
  padding: 1em;
  background-color: #000;
  color: #fff;
}
.body {
  background-color: #0ff;
  color: #000;
  container-type: inline-size;
}
.inner {
  display: grid;
  grid-template-rows: 1fr;
  height: 100%;
  min-height: 64px;
  max-height: 30cqh;
  overflow: clip;
}
.inner1 {
  display: block;
  overflow: hidden;
  width: 100%;
  height: 100%;
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
  object-fit: contain;
}

.window {
  position: fixed;
  top: 50vh;
  left: 50vw;
  width: 100px;
  height: 100px;
  background: #f00;
  opacity: 0.1;
  container-type: size;
}
</style>
