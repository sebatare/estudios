<template>
    <div class="flex p-8 justify-center">
        <input type="text" class="rounded border-2 border-gray-200 w-full" placeholder="Search for meals" />
        <div class="flex gap-1">
            <router-link to="/" v-for="letter of letters">
                {{ letter }}
            </router-link>
        </div>
    </div>
</template>
<script setup>


import { computed } from 'vue';
import store from '../store';

const meals = computed(() => store.state.meals)
const letters = 'ABCDEFGHJIKLMNOPQRSTUVWXYZ'.split('')


</script>