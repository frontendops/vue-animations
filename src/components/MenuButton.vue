<template>
    <span>
        <button
            class="menu-button"
            @click="toggleMenu">Open</button>
    </span>
</template>

<script>
export default {
    name: 'MenuButton',
    methods: {
        toggleMenu() {
            this.$emit('toggle-menu')
        }
    }
}
</script>

<style>
.menu-button {
    margin-left: 1rem;
    background-color: #3d84a8;
    color: white;
    padding: 0;
    border: none;
    font: inherit;
    padding: 0.4rem;
    border-radius: .5rem;
    /* show a hand cursor on hover; some argue that we
    should keep the default arrow cursor for buttons */
    cursor: pointer;
}
</style>
