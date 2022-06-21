<template>
  <section>
    <div>
      <h3>Advanced Statistics</h3>
      <p>
        Track how your links are performing accross the web with our advanced
        statistics dashboard
      </p>
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
@media screen and (min-width: 1024px) {
  section {
    padding: 13rem 4rem 10rem;
  }
}
h3 {
  font-size: 1.52rem;
  line-height: 1.2;
  color: var(--very-dark-violet);
}
p {
  color: var(--grayish-violet);
  margin-top: 10px;
}
button {
  margin-top: 2rem;
}
@media screen and (min-width: 768px) {
  h3 {
    font-size: 2rem;
  }
}
</style>
