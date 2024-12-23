<template>
    <div class="home">
        <button
          class="btn"
          @click="decrement"
        >-</button
        >
        <span class="counter">{{ count }}</span>
        <button
          class="btn"
          @click="increment"
        >+</button
        >
    </div>
</template>


<script setup>
    import { ref } from 'vue';
    
    const count = ref(0);
    const increment = () => count.value++;
    const decrement = () => count.value--;
</script>

<style scoped lang="scss">
    .home {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;
    }

    .btn {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        border: 1px solid #ccc;
        cursor: pointer;
    }

    .counter {
        font-size: 30px;
    }
</style>