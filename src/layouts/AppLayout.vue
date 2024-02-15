<template>
    <header >
        <slot name="top-layout"></slot>
    </header>
    <main class="container w-full mx-auto h-screen bg-slate-50">
        <slot name="content"></slot>
    </main>    
    <footer>

    </footer>
</template>

<script setup>

</script>