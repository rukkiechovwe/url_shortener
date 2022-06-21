<script setup lang="ts">
import UiStatistics from "../components/ui/uiStatistics.vue";
</script>
<template>
  <section>
    <h3>Advanced Statistics</h3>
    <p>
      Track how your links are performing accross the web with our advanced
      statistics dashboard
    </p>
    <div class="stat-container">
      <UiStatistics
        title="Brand Recognition"
        desc="Boost your brand recognition with
      each click. Generic links dont mean a thing.Branded links help instill confidence in your content"
        icon="icon-brand-recognition"
      />
      <UiStatistics
        title="Detailed Records"
        desc="Gain insights into who is clicking your links. Knowin when and where people engage with your content helps inform better decisions"
        icon="icon-detailed-records"
      />
      <UiStatistics
        title="Fully Customizable"
        desc="Improve brand awareness and content discoverablity through customizable links, supercharging audience engagement."
        icon="icon-fully-customizable"
      />
    </div>
  </section>
</template>
<style scoped>
section {
  min-height: 100vh;
  text-align: center;
  padding: 13rem 2rem 10rem;
  background-color: hsl(225, 33.3%, 95.3%);
  margin-top: -5rem;
}
.stat-container {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding-top: 3rem;
}

h3 {
  font-size: 1.52rem;
  line-height: 1.2;
}
button {
  margin-top: 2rem;
}
@media screen and (min-width: 1024px) {
  section {
    padding: 13rem 4rem 10rem;
  }
}
@media screen and (min-width: 768px) {
  h3 {
    font-size: 2rem;
  }
  .stat-container {
    display: flex;
    align-items: center;
    flex-direction: row;
  }
}
</style>
