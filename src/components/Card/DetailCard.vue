<template>
    <div class="relative w-80 -z-8 h-auto bg-red-300">
        <img class="relative" :src="imgSrc" />
        <div class="absolute w-full h-20 transition ease-out z-9 delay-5000 hover:-translate-y-10 bg-white bottom-0">
            Testt
            <div class="relative w-full h-auto -z-99 bg-blue-300">
                <shadow-button class="-z-99 " color="blue" text="Lihat Detail"></shadow-button>
            </div>
        </div>
    </div>    
</template>
<script setup>
    const props = defineProps({
        imgSrc:String
    })
    import ShadowButton from '@/elements/ShadowButton.vue';
</script>