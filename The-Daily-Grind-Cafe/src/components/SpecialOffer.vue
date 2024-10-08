<!--Conditional Rendering directives - v-if v-else -->
<!-- v-html -->
<script setup>
const isDiscountAvailable = false;
const htmlContent = "<i> Freshly brewed coffee, just for you! </i>";
</script>

<template>
  <div class="special">
    <h3>Special Offer</h3>
    <!-- Using v-html directive -->
    <p v-html="htmlContent"></p>
    <p v-if="isDiscountAvailable">Enjoy 20% Discount on all orders!</p>
    <p v-else>Enjoy 10% more Discount only for members</p>
  </div>
</template>

<style>
.special {
  text-align: center;
  padding: 20px;
  background-color: bisque;
  color: brown;
}
</style>
