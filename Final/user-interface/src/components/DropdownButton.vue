

<template>
  <div class="dropdown">
    <button @click="toggleDropdown" :style="buttonStyle">
      {{ buttonText }}
      <i :class="['arrow-icon', { 'arrow-up': isOpen, 'arrow-down': !isOpen }]"></i>
    </button>
    <transition name="fade">
      <div v-show="isOpen" class="dropdown-content">
        <slot></slot>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  props: {
    buttonText: {
      type: String,
      default: 'Dropdown',
    },
    buttonStyle: Object
  },
  methods: {
    toggleDropdown() {
      this.isOpen = !this.isOpen;
    },
    closeDropdown(event) {
      // Prevent the click event on the button from reaching the document
      event.stopPropagation();
      this.isOpen = false;
    },
  },
};
</script>

<style scoped>
/* Your existing styles remain unchanged */
</style>
