<template>
    <button :class="['base-button', { 'is-primary': primary }]" v-bind="$attrs">
        <slot />
    </button>
</template>

<script lang="ts" setup>
defineProps<{ primary?: boolean }>()
</script>

<style scoped>
.base-button {
    padding: 0.5em 1.2em;
    border-radius: 4px;
    border: none;
    background: #eee;
    color: #222;
    cursor: pointer;
    font-weight: 500;
    transition: background 0.2s;
}

.base-button.is-primary {
    background: #42b983;
    color: #fff;
}

.base-button:active {
    opacity: 0.85;
}
</style>