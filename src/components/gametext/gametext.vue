<template>
    <div id="text" v-html="text"></div>
</template>

<script setup>
defineProps([
    'text'
]);
</script>