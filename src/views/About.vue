<template>
    <div id="app">
        <p>Makanan khas-nya Jogja adalah {{ jogja }}</p>
        <p>Makanan khas-nya Makassar adalah {{ makassar }}</p>
    </div>
</template>

<script src="vue.js"></script>
    <script>
        new Vue ({
            el: '#app',
            data: {
                jogja: 'Gudeg',
                makassar: 'Coto'
            }
        });
    </script>

<style>
</style>