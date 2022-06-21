<script setup lang="ts">
import UiInput from "../components/ui/uiInput.vue";
import { ref, reactive } from "vue";

const urlLink = ref("");
const validateError = ref("");
interface Error {
  error: string | object | null;
}
const error: Error = reactive({ error: "" });
const loading = ref(false);
const shortenedLink = reactive({ result: null });

const handleSubmit = async () => {
  validateError.value = "";
  if (urlLink.value) {
    loading.value = true;
    try {
      const res = await fetch(
        ` https://api.shrtco.de/v2/shorten?url=${urlLink.value}`
      );
      const json = await res.json();
      if (res.status === 201) {
        shortenedLink.result = json.result;
      } else if (res.status === 400) {
        if (typeof json === "object") {
          error.error = json.error;
        }
      }
    } catch (err) {
      if (typeof err === "object") {
        error.error = err;
        console.log(error.error);
      }
    }
    loading.value = false;
  } else {
    validateError.value = "Please add a link";
    console.log(validateError.value);
  }
};
</script>
<template>
  <section>
    <div>
      <p v-if="error">{{ error.error }}</p>

      <UiInput
        v-model="urlLink"
        name="url"
        type="text"
        :error="validateError"
        placeholder="Shorten a link here..."
      />
      <button type="submit" @click.prevent="handleSubmit">
        {{ loading ? "loading..." : "Shorten It!" }}
      </button>
    </div>
  </section>
</template>
<style scoped>
section {
  position: relative;
  z-index: 99;
  width: 100%;
  padding: 2rem;
}
@media screen and (min-width: 1024px) {
  section {
    padding: 0 4rem;
  }
}
section > div {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  background: url("../assets/images/bg-shorten-mobile.svg");
  background-color: var(--dark-violet);
  background-position: top;
  background-repeat: no-repeat;
  background-size: contain;
  width: 100%;
  border-radius: 10px;
  padding: 1rem;
}

button {
  margin-top: 1rem;
  min-width: 100%;
  border-radius: 5px;
}
@media screen and (min-width: 768px) {
  section > div {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    background: url("../assets/images/bg-shorten-desktop.svg");
    background-color: var(--dark-violet);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    border-radius: 10px;
    padding: 3rem;
  }
  button {
    margin-top: 0;
    margin-left: 1rem;
    min-width: 180px;
    border-radius: 10px;
  }
}
</style>
