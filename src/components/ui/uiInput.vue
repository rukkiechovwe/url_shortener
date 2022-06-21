<script setup lang="ts">
import { ref, watch } from "vue";
interface Props {
  value?: string;
  name: string;
  type: string;
  placeholder?: string;
  error?: string;
}
const props = defineProps<Props>();

const url = ref(props.value);
const emit = defineEmits(["update:modelValue"]);
watch(url, (currentValue) => {
  emit("update:modelValue", currentValue);
});
</script>

<template>
  <div>
    <p v-if="error">
      <em>{{ error }}</em>
    </p>
    <input :type="type" v-model="url" :name="name" :placeholder="placeholder" />
  </div>
</template>
<style scoped>
div {
  width: 100%;
  display: flex;
  flex-direction: column-reverse;
}
p {
  color: var(--red);
  font-size: 14px;
  margin-top: 5px;
}
p + input{
   border: 2px solid var(--red)
}
</style>
