<script setup>
import {ref} from "vue"

const typInputu = ref("password");

function zmenTyp() {
    typInputu.value = "text";
}

const nazevOdkazu = ref("Nic");
const cilOdkazu = ref("#");
function zmenCilOdkazu(argNazev, argAdresa) {
    nazevOdkazu.value = argNazev;
    cilOdkazu.value = argAdresa;
}

const boolZakazany = ref(false);
function zakazInput() {
    boolZakazany.value = true;
}

</script>


<template>
    <h2>Direktiva v-bind</h2>

    <input v-bind:type="typInputu" name="" id="">
    <button @click="zmenTyp()">Zobrazit heslo</button>

    <hr>

    <div>
        <button @click="zmenCilOdkazu('Google', 'https://google.com')">
            Google
        </button>
        <button @click="zmenCilOdkazu('Seznam', 'https://seznam.cz')">
            Seznam
        </button>
        <button @click="zmenCilOdkazu('Primakurzy', 'https://primakurzy.cz')">
            Primakurzy
        </button>
        <br>
        <a :href="cislOdkazu" target="_blank">{{ nazevOdkazu }}</a>   
    </div>
    
    <hr>
    <input type="text" :disabled="boolZakazany">
    <button @click="zakazInput()">Zakazat input</button>

</template>


<style scoped></style>

