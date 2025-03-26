<template>
  <div class="qr-code-container">
    <qrcode-vue
        value="order"
        :level="M"
        :size="256"
        foreground="#000000"
        background="#FFFFFF"
        render-as="image" />
  </div>
</template>

<script>
import QrcodeVue from 'qrcode.vue';

export default {
  components: {
    QrcodeVue,
  },
  data() {
    return {
      qrCodeValue: `${window.location.origin}/order`
    };
  },
};
</script>

<style scoped>
.qr-code-container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}</style>