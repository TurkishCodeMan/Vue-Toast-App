<template>
  <div class="container">
    <button @click="toastCreate" class="btn btn-create">
      Create Toast Message
    </button>
    <app-toasts></app-toasts>
  </div>
</template>

<script>
import Toasts from "./Toasts";
import { eventBus } from "../eventBus";
export default {
  components: {
    appToasts: Toasts,
  },

  methods: {
    toastCreate() {
      let toast = {
        text: "Hoşgeldiniz",
        type: "warning",
      };
      eventBus.$emit("createToast", toast);
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}

.btn.btn-create {
  border-radius: 8px;
  padding: 1rem;
  border: none;
  color: #fff;
  background-color: rebeccapurple;
}

.btn:focus {
  outline: none;
}
</style>>

