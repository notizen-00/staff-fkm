<template>
    <nav class="flex container mt-10 ml-40" aria-label="Breadcrumb">
        <ol class="flex items-end space-x-3">
            <li>
               <i class="fal fa-home"></i> <a href="/" class="text-gray-600 hover:text-gray-900">Home</a>
            </li>
            <li>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400" viewBox="0 0 20 20"
                    fill="currentColor">
                    <path fill-rule="evenodd"
                        d="M9.293 5.293a1 1 0 011.414 0l4 4a1 1 0 01-1.414 1.414L10 7.414l-3.293 3.293a1 1 0 01-1.414-1.414l4-4zM5 10a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1z"
                        clip-rule="evenodd" />
                </svg>
            </li>
            <li>
                <a :href="secondUrl" class="text-gray-600 hover:text-gray-900">{{ secondBar }}</a>
            </li>
            <li>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400" viewBox="0 0 20 20"
                    fill="currentColor">
                    <path fill-rule="evenodd"
                        d="M9.293 5.293a1 1 0 011.414 0l4 4a1 1 0 01-1.414 1.414L10 7.414l-3.293 3.293a1 1 0 01-1.414-1.414l4-4zM5 10a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1z"
                        clip-rule="evenodd" />
                </svg>
            </li>
            <li>
                <span class="text-gray-900">{{ currentBar }}</span>
            </li>
        </ol>
    </nav>

</template>
<script setup>
    const props = defineProps({
        secondBar:String,
        secondUrl:String,
        currentBar:String,
    })
</script>