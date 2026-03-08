<script setup>
</script>

<template>
    <header>
        <div>
            <nav>
                <NuxtLink to="/">Home</NuxtLink>
                <NuxtLink to="/projects">Projects</NuxtLink>
                <NuxtLink to="/contact">Contact</NuxtLink>
            </nav>
            <slot />
        <hr/>
        </div>
    </header>
</template>

<style scoped>
nav{
    font-family: Arial, Helvetica, sans-serif;
    background-color: white;
    padding: 30px;
    display: flex;
    justify-content: center;
    gap: 200px;
}

nav a:hover {
    color: #2563eb;
    background-color: #f1f5f9
}

nav a:active {
    color: #2563eb;
}
</style>