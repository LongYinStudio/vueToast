<template>
  <div>
    <button @click="show">弹框</button>
    <Toast ref="Toast"></Toast>
  </div>
</template>

<script>
import Toast from "./components/Toast.vue";
export default {
  components: { Toast },
  methods: {
    show() {
      this.$refs.Toast.showToast("test", 1000);
    },
    comments: {
      Toast,
    },
  },
};
</script>
