<template>
    <v-container class="fill-height">
        <v-btn color="primary" dark slot="activator">About me
            <v-menu activator="parent">
                <v-list>
                    <v-list-item v-for="(item, index) in items" :key="index" :value="index">
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item>
                </v-list>
            </v-menu>
        </v-btn>

    </v-container>
</template>
  
<script setup>
import { ref } from 'vue'

const items = ref([
    { title: 'Tab 1' },
    { title: 'Tab 2' }
]) 
</script>
  