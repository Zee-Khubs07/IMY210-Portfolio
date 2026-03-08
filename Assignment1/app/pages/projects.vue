<script setup>
</script>

<template>
    <!--Zinathi Khuboni, u25181302-->
    <div>
        <h1>My Projects</h1>
        <p id = "projects">Here are some of the projects I have completed at the University of Pretoria:</p>

        <section>
            <h2>1. Isometric Room Artwork(IMY 120)</h2>
            <p>For this assignment, I designed a digital artwork of a room using isometric perspective. I focused on creating clean shapes to capture the furniture and layout of my living room in a stylised way.</p>
        </section>

        <section>
            <h2>2. Haunted Forest Animation(IMY 120)</h2>
            <p>For this project, I created a scary environment. It includes a haunted forest with moving tree branches, ghosts floating in the fog and bats flying. I also made use of Adobe Audition to add sound effects to make it feel more exciting.</p>
        </section>

        <section>
            <h2>3. Personal Brand Logo(IMY 120)</h2>
            <p>I designed a logo that represents my personal brand in Adobe Illustrator.</p>
        </section>
    </div>
    
</template>

<style scoped>
    div {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #f1f5f9;
        color: #1f2937;
        min-height: 900px;
    }

    h1 {
        text-align: center;
        margin-bottom: 10px;
        color: #111827;
        text-decoration: underline;
        padding: 30px;
    }

    h2 {
        text-decoration: underline;
        text-align: center;
    }

    section {
        background-color: white;
        margin: 0 auto 40px auto;
        padding: 40px;
        max-width : 800px;
        border: 1px solid black;
        box-shadow: 8px 8px;
        border-radius: 24px;
    }

    section:hover{
    transform: translateY(-5px)
    }

    #projects {
        text-align: center;
    }

    p {
        color: black;
    }
</style>