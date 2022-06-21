<template>
  <section>
    <h3>Boost your links today</h3>
    <button>Get Started</button>
  </section>
</template>
<style scoped>
section {
  position: relative;
  z-index: 99;
  width: 100%;
  padding: 3rem;
  text-align: center;
  background: url("../assets/images/bg-boost-mobile.svg");
  background-color: var(--dark-violet);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 2rem;
}

h3 {
  font-size: 1.52rem;
  line-height: 1.2;
  color: var(--white);
}
button {
  margin-top: 2rem;
}
@media screen and (min-width: 1024px) {
  section {
    padding: 4rem;
  }
}
@media screen and (min-width: 768px) {
  section {
    background: url("../assets/images/bg-boost-desktop.svg");
    background-color: var(--dark-violet);
    padding: 4rem;
  }
  h3 {
    font-size: 2rem;
  }
}
</style>
