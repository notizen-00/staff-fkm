<template>
    <AppLayout>
    <template #top-layout>
        <Navbar></Navbar>
    </template>
    <template #content>
        <breadcrumb secondBar="Staff" secondUrl="#" currentBar="List Staff"></breadcrumb>
        <div class="w-full ml-40 mt-10 flex justify-items-stretch">
            <div class="w-2/3">
                <konten></konten>
            </div>
            <div class="w-1/4">
                <ListMenu></ListMenu>
            </div>
        </div>
        <section id="dosen" class="w-full ml-40">
        <Kategori class="mb-10"></Kategori>
        <card-dosen></card-dosen>
        </section>
    </template>
    </AppLayout>
</template>
<script setup>
    import Kategori from '@/components/kategori/kategori.vue'
    import Navbar from '@/containers/Navbar.vue';
    import AppLayout from '@/layouts/AppLayout.vue';
    import breadcrumb from '@/components/breadcrumb/breadcrumb.vue';
    import konten from '@/components/konten/konten.vue';
    import ListMenu from '@/components/ListMenu/ListMenu.vue';
    import CardDosen from '@/containers/CardDosen.vue';
</script>