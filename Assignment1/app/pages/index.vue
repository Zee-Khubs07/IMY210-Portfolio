<script setup>
import { ref } from 'vue'
const catFact = ref("")
const weather = ref("")

async function getRandomFacts(){
    try{
        const response = await fetch('https://meowfacts.herokuapp.com/');
    if(response.ok){
        const data = await response.json();
        catFact.value = data.data[0];
        console.log(data);
    } else {
        throw new Error('Failed to fetch data');
    }
} catch (error){
    console.error('Error:', error);
    }
}

getRandomFacts()

async function getWeatherForecast(){
    try{
        const response = await fetch('https://api.open-meteo.com/v1/forecast?latitude=-25.74&longitude=28.18&current=temperature_2m,wind_speed_10m&hourly=temperature_2m,relative_humidity_2m,wind_speed_10m');
    if(response.ok){
        const data = await response.json();
        weather.value = {
            temperature: data.current.temperature_2m + "°C",
            wind: data.current.wind_speed_10m + " km/h",
            description: "Live from Pretoria",
            time: data.current.time,
        };
        console.log(data);
    } else {
        throw new Error('Failed to fetch data');
    }
} catch (error){
    console.error('Error:', error);
    }
}

getWeatherForecast()

</script>


<template>
    <!--Zinathi Khuboni, u25181302-->
    <div id ="bio">
        <h1>Welcome to my Portfolio</h1>
        <h2 id ="name">Chumani Zinathi Khuboni</h2>
        <section>
            <img src = "/Zee.jpeg" alt="Me" width = "50%">
            <p>I am currently a second year Multimedia student at the university of pretoria,
                pursuing a degree in BIS Multimedia. I am aspiring to become either a programmer or website developer.
            </p>

            <p>
                Even though I originally wanted to study electrical engineering, I have discovered a new passion for coding and developing websites.
            </p>

            <p>
                I love to dance outside of my school work. Dancing is my favourite way to clear my mind.
            </p>
        </section>

        <section>
            <div v-if="catFact">
                <h2>Random Fact About Cats</h2>

                <h3>Did you know?</h3>
                <p>{{ catFact }}</p>
            </div>
        </section>

        <section>
            <div v-if="weather">
                <h2>Weather Forecast:</h2>
                <p>Temperature: {{ weather.temperature }} </p>
                <p>Wind: {{ weather.wind }} </p>
                <p>Description: {{ weather.description }} </p>
                <p>Time: {{ weather.time }} </p>
            </div>
        </section>
    </div>
</template>

<style scoped>
#bio{
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f1f5f9;
    color: #1f2937;
    max-width: 100%;
    min-height: 1500px;
}



section{
    background-color: white;
    color: black;
    padding: 30px;
    border: 1px solid black;
    border-radius: 24px;
    margin: 0 auto 40px auto;
    box-shadow: 8px 8px;
    max-width: 800px;
    width: 100%;
}

section:hover{
    transform: translateY(-5px)
}

#name {
    text-align: center;
}

img {
    border: 1px solid black;
    border-radius: 15px;
    display: block;
    max-height: 500px;
    max-width: 500px;

}

h3 {
    margin-top: 10px;
    color: #2563eb;
}

h1 {
    text-align: center;
    padding: 30px;
    text-decoration: underline;
    color: #111827;
}

h2 {
    text-decoration: underline;
    color: #1f2937;
    margin-bottom:10px;
}

</style>