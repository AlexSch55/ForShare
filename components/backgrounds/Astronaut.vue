<template>
    <div
        class="absolute inset-0 w-full h-full -z-10 bg-cover bg-center bg-no-repeat"
        :style="`background-image: url('${Background}')`"
    >
    </div>
</template>

<script setup lang="ts">
import Background from "@/assets/images/background.png"
</script>