<template>
    <div id="Control">
        <button v-on:click="onClick(0)">{{ buttons[0] }} </button>
        <button v-on:click="onClick(1)">{{ buttons[1] }} </button>
        <button v-on:click="onClick(2)">{{ buttons[2] }} </button>
    </div>
</template>

<script setup>


defineProps(['buttons']);
const emit = defineEmits(['action']);
function onClick(index){
emit('action',index)
};
</script>