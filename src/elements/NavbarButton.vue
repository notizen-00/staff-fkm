<template>
    <a :href="url" style="font-family:Libre Karville;"
    class="text-slate-600 active active:border-t-4 active:border-red-300 hover:border-b-4 hover:border-red-400 hover:text-slate-900  px-3 py-2 font-medium text-2xl">{{ text }}</a>
</template>
<script setup>
    const props = defineProps({
        text: String,
        url: {
            type: String,
            default: '#'
        }
    });
</script>