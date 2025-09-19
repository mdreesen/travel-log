<script lang="ts" setup>

const colorMode = useColorMode();

const isDark = computed({
    get() {
        return colorMode.value === 'dark';
    },
    set(value) {
        return colorMode.preference = value ? 'dark' : 'light';
    }
})

</script>

<template>
    <label className="swap swap-rotate mx-4">
        <!-- this hidden checkbox controls the state -->
        <input v-model="isDark" type="checkbox" >

        <!-- sun icon -->
        <baseThemeIcon styles="swap-on" icon-name="tabler:sun" />

        <!-- moon icon -->
        <baseThemeIcon styles="swap-off" icon-name="tabler:moon" />
    </label>
</template>