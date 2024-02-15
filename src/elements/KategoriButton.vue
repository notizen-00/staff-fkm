<template>
    <div class="kotak w-full text-center font-bold font-sans ml-2">
    <button class="font-semibold text-xl font-libre mt-6">{{ text }}</button><br>
    <h1>{{subtitle}}</h1>
    </div>
</template>

<script setup>
    const props = defineProps({
        text:String,
        subtitle:String,
    })
</script>

<style>
    .font-libre {
        font-family: Libre Karsville;
       
    }
    div.kotak {
        height: 0px;
        color:blue;
        background: white;
        transition: height 0.4s ease-in-out, background 0.1s ease-in-out, color 0.5s ease-in-out;
        border-top: 5px solid rgb(71, 68, 238);
    }

    div.kotak:hover {
        height: 100px;
        color: white;
        background: rgb(13, 8, 28);
        border: 1px solid black;
    }

    div.kotak.active {
        --tw-text-opacity: 1;
        color: white;
        height: 100px;
        background: rgb(13, 36, 165);
    }
</style>