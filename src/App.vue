<script setup lang="ts">
import ShortenLink from "./components/ShortenLink.vue";
import HeroSection from "./components/HeroSection.vue";
import MoreInfo from "./components/MoreInfo.vue";
import BoostSection from "./components/BoostSection.vue";
import NavBar from "./components/NavBar.vue";
</script>

<template>
  <main>
    <NavBar />
    <HeroSection />
    <ShortenLink />
    <MoreInfo />
    <BoostSection />
  </main>
</template>

<style>
@import "./assets/base.css";
</style>
