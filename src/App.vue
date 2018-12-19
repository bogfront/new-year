<template>
    <div id="app">
        <div class="container">
            <Cover :host="host"/>
            <Stat :year="year"/>
            <hr>
            <Stat :month="month"/>
            <hr>
            <Stat :time="time"/>
            <hr>
            <Stat :day="day"/>
            <Stat :channel="channel"/>
            <Footer/>
        </div>
    </div>
</template>

<script>

    import Cover from "./components/Cover";
    import Stat from "./components/Stat";
    import Footer from "./components/Footer";

    export default {
        name: 'app',
        components: {
            Footer,
            Stat,
            Cover

        },
        data() {
            return ({
                host: {
                    name: 'Хостнейм',
                    logo: '/img/logohost.png',
                    eventsCovers: ['/img/cover1.png', '/img/cover2.png']
                },
                year: {
                    events: 114,
                    tickets: 2113444,
                    money: 203113444
                },
                month: 'Июль',
                time: '17:00',
                day: 'Пятница',
                channel: 'Виджет, касса и билетный стол'
            });
        }
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Roboto:400,700');

    body {
        font-family: 'Roboto', sans-serif;
    }

    button {
        border: none;
        box-shadow: none;
    }

    hr {
        border: none;
        border-bottom: 1px solid #e5e5e5;
        width: 80%;
    }

    .container {
        width: 1200px;
        margin: 280px auto;
        background: #fff;
        border-radius: 10px;
        box-shadow: 0 30px 100px rgba(0, 0, 0, 0.3);
    }

    .title {
        font-size: 40px;
        line-height: 50px;
        font-weight: 700;
        color: #111;
        margin-bottom: 30px;
    }
    .subtitle {
        opacity: 0.8;
        color: #000000;
        font-size: 22px;
        font-weight: 400;
        line-height: 30px;
    }

    .btn {
        color: #fff;
        font-size: 18px;
        font-weight: 500;
        line-height: 50px;
        border-radius: 25px;
        background: #466eff;
        padding: 0 32px;
        cursor: pointer;
        transition: background .2s;
    }
    .btn:hover {
        background: #0b4fff;
    }
</style>
