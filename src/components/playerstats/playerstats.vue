<template>

<div id="stats">
<span class="stats">XP:<strong>{{ xp }}</strong></span>
<span class="stats">Health:<strong>{{ health }}</strong></span>
<span class="stats">Gold:<strong>{{ gold }}</strong></span>

</div>

</template>

<script setup>
defineProps([
    'xp',
    'health',
    'gold'
]);

</script>