<template>
  <nav>
    <ul class="img">
      <img src="../assets/images/logo.svg" />
      <ul>
        <li><a href="#">Features</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">Resources</a></li>
      </ul>
    </ul>
    <ul>
      <li><a href="#">Login</a></li>
      <li><button>Sign up</button></li>
    </ul>
  </nav>
</template>
<style scoped>
nav {
  display: none;
  align-items: center;
  justify-content: space-between;
  padding: 2rem 2rem;
}
@media screen and (min-width: 1024px) {
  nav {
    padding: 2rem 4rem;
  }
}
@media screen and (min-width: 768px) {
  nav {
    display: flex;
  }
}
ul {
  display: flex;
  align-items: center;
  list-style: none;
}
a {
  display: block;
  padding: 0 1.2rem;
  font-weight: 700;
}
a:hover {
  color: var(--very-dark-violet);
}

h1 {
  font-size: 4rem;
  line-height: 1.2;
  color: var(--very-dark-violet);
}
p {
  color: var(--grayish-violet);
}
button {
  padding: 7px 1rem;
}
</style>
