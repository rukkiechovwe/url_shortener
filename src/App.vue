<script setup lang="ts">
import ShortenLink from "./components/ShortenLink.vue";
import HeroSection from "./components/HeroSection.vue";
import AdvancedStatistics from "./components/AdvancedStatistics.vue";
import BoostSection from "./components/BoostSection.vue";
import NavBar from "./components/NavBar.vue";
import FooterSection from "./components/FooterSection.vue";
</script>

<template>
  <main>
    <NavBar />
    <HeroSection />
    <ShortenLink />
    <AdvancedStatistics />
    <BoostSection />
    <FooterSection />
  </main>
</template>

<style>
@import "./assets/base.css";
</style>
