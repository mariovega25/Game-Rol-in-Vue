<template>
<div id="monsterStats" v-if="visible">
<span class="stat">Monster Name:<strong>{{ name }}</strong></span>
<span class="stat">Health: <strong>{{ health }}</strong></span>
</div>

</template>
<script setup>

defineProps(['name','health','visible']);

</script>