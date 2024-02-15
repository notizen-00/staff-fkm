<template>

    <div class="w-2/3 flex justify-items-center mt-10">
        <kategori-button text="Gizi" :class="{active: activeItem === 1}" @click="toggleActive(1)"></kategori-button>
        <kategori-button text="Kesehatan" subtitle="Masyarakat" :class="{active: activeItem === 2}" @click="toggleActive(2)"></kategori-button>
        <kategori-button text="Administrasi" subtitle="Kesehatan" :class="{active: activeItem === 3}" @click="toggleActive(3)"></kategori-button>


    </div>

</template>

<script setup>
    import {
        ref
    } from 'vue'
    import KategoriButton from '@/elements/KategoriButton.vue';
    defineProps({
        msg: String,
    })

    const count = ref(0)

    const activeItem = ref(1)

    const toggleActive = (index) => {
        activeItem.value = activeItem.value === index ? null : index
    }
</script>

