<template>
    <span>{{listing.street}} {{listing.streent_nr}}, {{listing.city}}</span>
</template>

<script setup>
 defineProps({
     listing: Object
 })

</script>
