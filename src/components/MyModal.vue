<script setup>
import { ref } from 'vue'

const open = ref(false)

</script>

<template>
    <button @click="(open = !open)">Open Modal</button>

    <Teleport to="body">
        <div v-if="open" class="modal">
            <p>Hello</p>
            <button @click="(open = !open)">Close</button>
        </div>
    </Teleport>
</template>

<style scoped>
.modal {
    position: fixed;
    z-index: 999;
    top: 20%;
    left: 50%;
    width: 300px;
    margin-left: -150px;
    padding: 20px 30px;
    border-radius: 5px;
    background: #ddd;
}
</style>