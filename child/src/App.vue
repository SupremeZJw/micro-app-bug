<template>
  <div>
    <a-button type="primary" @click="showModal">Open Modal</a-button>
    <Modal v-if="open" @onCancel="handleOk" />
  </div>
</template>
<script setup>
import { ref } from 'vue';
import Modal from './modal.vue'
const open = ref(false);
const showModal = () => {
  open.value = true;
};
const handleOk = e => {
  open.value = false;
};
</script>