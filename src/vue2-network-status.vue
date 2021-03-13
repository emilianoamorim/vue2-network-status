<template>
  <div v-if="!isOnline">
    <slot v-if="hasSlot()" />
    <p v-if="!hasSlot()">You are offline!</p>
  </div>
</template>

<script>
export default /*#__PURE__*/ {
  name: "Vue2NetworkStatus", // vue component name
  data: () => ({
    isOnline: navigator.onLine || false,
    eventListeners: ["online", "offline"],
  }),
  created() {
    this.eventListeners.forEach((e) =>
      window.addEventListener(e, this.currentStatus)
    );
  },
  beforeDestroy() {
    this.eventListeners.forEach((e) =>
      removeEventListener(e, this.currentStatus)
    );
  },
  methods: {
    currentStatus() {
      this.isOnline = navigator.onLine || false;
      this.$emit("current-status", this.isOnline);
    },
    hasSlot(name = "default") {
      return !!this.$slots[name] || !!this.$scopedSlots[name];
    },
  },
};
</script>

<style scoped></style>
