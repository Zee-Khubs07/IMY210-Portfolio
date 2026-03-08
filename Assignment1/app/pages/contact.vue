<script setup>
</script>

<template>
    <!--Zinathi Khuboni, u25181302-->
    <div id = "contacts">
        <h1>Contact Me</h1>
        <form name = "contact" method= "POST" data-netlify = "true">

            <input type = "hidden" name = "form-name" value = "contact" />
            <p>
                <label>Name: <input type = "text" name = "name" /></label>
            </p>

            <p>
                <label>Email: <input type = "email" name = "email" /></label>
            </p>

            <p>
                <label>Message: <textarea name = "message" ></textarea></label>
            </p>

            <p>
                <button type = "submit">Send</button>
            </p>

        </form>
    </div>
</template>

<style scoped>
    #contacts {
        background-color: #f9f9f9;
        max-width: 600px;
        margin: 50px auto;
        border: 1px solid #ddd;
        text-align: center;
        border-radius: 15px;
        box-shadow: 8px 8px;
    }

    input, textarea {
        width: 80%;
        margin-top: 6px;
        padding: 10px;
        border: 1px solid #ddd;
        border-radius: 5px;
        display: inline-block;
    }

    h1 {
        color: #1f2937;
        margin-bottom: 20px;
    }

    label {
        display: block;
        margin-bottom: 20px;
        font-weight: bold;
    }


    p {
        color: #1f2937;
    }

    button {
        padding: 11px 22px;
        background-color: #1f2937;
        color: white;
        border-radius:4px;
        cursor: pointer;
    }

    button:hover {
        background-color: #374151;
    }

    a {
        color: #007bff;
    }
</style>