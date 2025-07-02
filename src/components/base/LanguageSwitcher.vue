<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import { ref, onMounted, onBeforeUnmount } from 'vue'

const { locale } = useI18n()
const languages = [
    { code: 'en', label: 'English', flag: '🇬🇧' },
    { code: 'nl', label: 'Dutch', flag: '🇳🇱' },
]
const open = ref(false)
const switcherRef = ref<HTMLElement | null>(null)

function selectLanguage(code: string) {
    locale.value = code
    open.value = false
}

function handleClickOutside(event: MouseEvent) {
    if (open.value && switcherRef.value && !switcherRef.value.contains(event.target as Node)) {
        open.value = false
    }
}

onMounted(() => {
    document.addEventListener('click', handleClickOutside)
})
onBeforeUnmount(() => {
    document.removeEventListener('click', handleClickOutside)
})
</script>

<template>
    <div class="lang-switcher" ref="switcherRef">
        <button class="lang-btn" @click="open = !open" type="button">
            <span class="globe">🌐</span>
            <span class="lang-label">{{languages.find(l => l.code === locale)?.label || locale}}</span>
            <span class="arrow" :class="{ open }">▼</span>
        </button>
        <transition name="fade">
            <ul v-if="open" class="lang-list">
                <li v-for="lang in languages" :key="lang.code" @click="selectLanguage(lang.code)"
                    :class="{ active: locale === lang.code }">
                    <span class="flag">{{ lang.flag }}</span>
                    <span class="label">{{ lang.label }}</span>
                    <span v-if="locale === lang.code" class="check">✔</span>
                </li>
            </ul>
        </transition>
    </div>
</template>

<style scoped>
.lang-switcher {
    position: relative;
    display: inline-block;
    margin-left: 1rem;
    font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
}

.lang-btn {
    background: #fff;
    border: 2px solid #2563eb;
    color: #222;
    padding: 0.5em 1.2em;
    border-radius: 2em;
    cursor: pointer;
    font-size: 1.08em;
    font-weight: 600;
    display: flex;
    align-items: center;
    gap: 0.7em;
    box-shadow: 0 2px 8px rgba(37, 99, 235, 0.08);
    transition: border 0.2s, box-shadow 0.2s;
    outline: none;
}

.lang-btn:hover,
.lang-btn:focus {
    border-color: #1d4ed8;
    box-shadow: 0 4px 16px rgba(37, 99, 235, 0.15);
}

.globe {
    font-size: 1.2em;
    color: #2563eb;
    filter: drop-shadow(0 1px 1px #b3c6ff);
}

.lang-label {
    font-weight: 600;
    letter-spacing: 0.01em;
}

.arrow {
    font-size: 0.9em;
    margin-left: 0.2em;
    transition: transform 0.2s;
    color: #2563eb;
}

.arrow.open {
    transform: rotate(180deg);
}

.lang-list {
    position: absolute;
    top: 120%;
    left: 0;
    background: #fff;
    border: 2px solid #2563eb;
    border-radius: 1em;
    box-shadow: 0 8px 32px rgba(37, 99, 235, 0.13);
    min-width: 170px;
    z-index: 10;
    padding: 0.4em 0;
    margin-top: 0.2em;
    animation: fadeIn 0.2s;
}

.lang-list li {
    display: flex;
    align-items: center;
    gap: 0.7em;
    padding: 0.7em 1.2em;
    cursor: pointer;
    font-size: 1.05em;
    font-weight: 500;
    color: #222;
    background: transparent;
    border: none;
    transition: background 0.18s, color 0.18s;
    border-radius: 0.7em;
    position: relative;
}

.lang-list li.active {
    background: #e0e7ff;
    color: #2563eb;
    font-weight: 700;
}

.lang-list li:hover {
    background: #f1f5ff;
    color: #1d4ed8;
}

.flag {
    font-size: 1.2em;
}

.check {
    margin-left: auto;
    color: #2563eb;
    font-size: 1.1em;
}

.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.2s;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(-10px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}
</style>