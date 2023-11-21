<template>
    <div class="parent-element">
        <select @change="input = $event.target.value" class="form-select">
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
        </select>
    </div>
    <p v-if="input == '1'" class="text-blue-500 font-bold">I Like you</p>
    <p v-else-if="input == '2'" class="text-pink-500 font-bold">I Hate you</p>
    <p v-else class="text-green-500 font-bold">Others</p>
</template>

<script setup>
import { ref } from 'vue';
const input = ref('1')
</script>

<style scoped>
.form-select {
    padding: 0.5rem;
    border-radius: 0.25rem;
    border: 10px solid #e5e7eb;
    margin: 0 auto;
    display: block;
}

.parent-element {
    display: flex;
    justify-content: center;
    align-items: center;
}

.text-blue-500 {
    color: #3b82f6;
}

.text-pink-500 {
    color: #ec4899;
}

.text-green-500 {
    color: #10b981;
}

.font-bold {
    font-weight: bold;
}</style>
