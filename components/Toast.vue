<template>
  <div v-if="show" class="toast">{{ message }}</div>
</template>

<script>
export default {
  name: "Toast",
  data() {
    return {
      show: false,
      message: "",
      timer: null,
    };
  },
  methods: {
    showToast(message, duration = 2000) {
      this.show = true;
      this.message = message;
      clearTimeout(this.timer);
      this.timer = setTimeout(() => {
        this.show = false;
      }, duration);
    },
  },
};
</script>

<style scoped>
.toast {
  position: fixed;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  padding: 10px 20px;
  background-color: rgba(0, 0, 0, 0.7);
  color: #fff;
  border-radius: 5px;
}
</style>
