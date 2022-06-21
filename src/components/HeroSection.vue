<template>
  <section>
    <div>
      <h1>More than just shorted links</h1>
      <p>
        Buiuld your brand's recognition and get detailed insights on how your
        links are performing
      </p>
      <button type="submit">Get Started</button>
    </div>
    <div class="img">
      <img src="../assets/images/illustration-working.svg" />
    </div>
  </section>
</template>
<style scoped>
section {
  display: flex;
  align-items: center;
  position: relative;
  padding: 5rem 2rem;
  flex-direction: column-reverse;
  text-align: center;
}
section > div {
  width: 100%;
}
section > .img {
  margin-bottom: 2rem;
}
section > .img > img {
  width: 144%;
}

h1 {
  font-size: 2.3rem;
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
@media screen and (min-width: 1024px) {
  section {
    padding: 10rem 4rem;
  }
}
@media screen and (min-width: 768px) {
  section {
    flex-direction: row;
    text-align: left;
    padding: 10rem 2rem;
  }
  section > div {
    width: 50%;
  }
  section > .img {
    position: absolute;
    right: -5rem;
    margin-bottom: 0;
  }
  section > .img > img {
    width: 100%;
  }
  h1 {
    font-size: 4rem;
    line-height: 1.2;
    color: var(--very-dark-violet);
  }
  p {
    max-width: 70%;
  }
}
</style>
