<template>
  <div class="toasts">
    <app-toast
      v-for="toast in toasts"
      :key="toast.index"
      :toast="toast"
    ></app-toast>
  </div>
</template>

<script>
import { eventBus } from "../eventBus";
import Toast from "./Toast";
export default {
  data() {
    return {
      toasts: [],
    };
  },

  components: {
    appToast: Toast,
  },

  mounted() {
    eventBus.$on("createToast", (toast) => {
      this.toasts.push(toast);

      setTimeout(() => {
        this.toasts.pop(toast);
      }, 2000);
    });
  },
};
</script>

<style scoped>
.toasts {
  position: fixed;
  right: 0;
  bottom: 0;
}
</style>