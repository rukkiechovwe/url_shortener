<script setup lang="ts">
interface Props {
  title: string;
  desc: string;
  icon: string;
}
const props = defineProps<Props>();
</script>
<template>
  <div class="container">
    <div class="top-icon">
      <img :src="`../../src/assets/images/${icon}.svg`" />
    </div>
    <h5>{{ title }}</h5>
    <p>{{ desc }}</p>
  </div>
</template>
<style scoped>
.container {
  background: var(--white);
  padding: 4rem 2rem 2rem;
  text-align: left;
  position: relative;
  margin: 3rem 0;
  border-radius: 5px;
  width: 100%;
  z-index: 99;
  margin-top: 2rem;
}
.container::after {
  content: "";
  position: absolute;
  background-color: var(---cyan);
  width: 10px;
  height: 80px;
  left: 50%;
  bottom: -80px;
  z-index: 11;
}
.container:first-child {
  margin-left: 0;
  /* margin-top: 0; */
}

.container:last-child {
  margin-right: 0;
}
.container:last-child::after {
  background-color: transparent;
}
h5 {
  font-size: 1.3rem;
  line-height: 1.2;
}
.top-icon {
  position: absolute;
  top: -30px;
  left: calc(50% - 30px);
  background-color: var(--dark-violet);
  border-radius: 50%;
  width: 70px;
  height: 70px;
  padding: 0.8rem;
}
@media screen and (min-width: 768px) {
  h5 {
    font-size: 1.6rem;
  }
  .container {
    margin: 3rem 15px;
    margin-top: 6rem;
  }
  .container::after {
    width: 80px;
    height: 10px;
    left: auto;
    right: -80px;
    top: 100px;
  }
  .container:first-child {
    margin-left: 0;
    margin-top: 0;
  }

  .container:last-child {
    margin-right: 0;
    margin-top: 12rem;
  }
  .top-icon {
    left: 25px;
  }
}
</style>
