<template>
  <div>Index from vue</div>
  <div>
    <p>the message is {{ message }}</p>
  </div>
</template>

<script setup>

defineProps({
  message:String,
})
</script>


