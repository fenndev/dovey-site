<script lang="ts">
export default {
    props: {
        to: {
            type: String,
            required: true
        },
        icon: {
            type: String,
            required: true,
            default: ''
            
        },
        iconAltText: {
            type: String,
            required: true,
            default: 'An img!!!'
        },
        linkText: {
            type: String,
            required: true,
            default: 'A link!!!'
        }
    }
}
</script>

<template>
  <a :href="to" >
    <img :src="icon" :alt="iconAltText">
    <p>{{linkText}}</p>
  </a>
</template>

<style scoped>
a {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    justify-content: space-evenly;
    align-items: center;
    width: 250px;
    height: 50px;
    border: 1px solid black;
    border-radius: 10px;
    margin: 10px;
    padding: 20px;
}

a, a:visited {
  color: black;
  text-decoration: none;
}

a:hover {
    background-color: #42b983;
    color: #e8f5e9;
}

img {
    width: 35px;
    height: 35px;
}

p {
    text-align: center;
    margin: 0;
    font-size: 1.5rem;
}
</style>