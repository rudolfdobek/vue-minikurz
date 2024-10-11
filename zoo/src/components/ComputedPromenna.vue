<script setup>
import {ref, computed} from "vue"

const polomer = ref(0);

setInterval(() => {
    polomer.value = Math.floor(Math.random() * 100);
}, 3000);

//computed je reactivni promenna ktera je zavila na jine reaktvni promenne
const obvod = computed(() => {
    const vysledek = 2 * polomer.value * Math.PI;
    return vysledek;
});

</script>

<template>
    <h2>Computed</h2>
    <p>Polomer kruhu: {{polomer}}</p>
    <p>Obvod kruhu: {{obvod}}</p>
</template>


<style scoped></style>