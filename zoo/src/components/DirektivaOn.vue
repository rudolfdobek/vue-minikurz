<script setup>
import {ref} from "vue"

const cislo = ref(0);

function odeber1() {
    cislo.value--;
}

</script>

<template>
    <h2>Direktiva: v-on</h2>

    <div>
        {{ cislo }}
    </div>

    <div>
        <button v-on:click="cislo++">Pridat 1</button>
        <button @click="odeber1()">Odebrat 1</button>
    </div>
</template>

<style scoped></style>