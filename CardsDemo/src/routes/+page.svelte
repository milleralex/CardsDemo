<script>
    let cards = [0, 1, 2]
    let dogs = [0, 2, 1 ,3]
</script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css" integrity="sha512-MV7K8+y+gLIBoVD59lQIYicR65iaqukzvf/nwasF0nqhPay5w/9lJmVM2hMDcnK1OnMGCdVK+iQrJ7lzPJQd1w==" crossorigin="anonymous" referrerpolicy="no-referrer" />
<div class="card_swiper">
<div class="cards_group">
{#each cards as card}
    <div class="card_group" data-index="{card}" data-status="{card !== 0 ? 'unknown' : 'active'}">
        {#each dogs as dog}
            <div class="card little_card"></div>
            <div class="card big_card"></div>
        {/each}
    </div>
{/each}
</div>
    <div class="card_swiper_buttons">
        <button id="hate">
            <i class="fa-solid fa-x"></i>
        </button>
        <button id="love">
            <i class="fa-solid fa-heart"></i>
        </button>
    </div>
</div>

<style>
    body {
        margin: 0;
        background-color: black;
    }
    button {
        font-size: 2.5vmin;
        border: 0.4vmin solid rgb(200, 200, 200);
        border-radius: 100%;
        color: white;
        background-color: transparent;
        height: 7vmin;
        width: 7vmin;
        cursor: pointer;
    }

    #love {
        color: rgb(33, 150, 243);
        border-color: rgb(33, 150, 243);
    }
    #hate {
        color: rgb(200, 0, 33);
        border-color: rgb(200, 0, 33);
    }
    .card_swiper_buttons {
        margin-top: 60vmin;
        display: flex;
        justify-content: space-around;
    }
    .card_group,
    .big_card{
        width: 30vmin;
        transition: transform 1s cubic-bezier(.05, .43, .25, .95);
    }
    .card_group[data-status="unknown"] {
        transform: scale(0);
    }

    .card {
        aspect-ratio: 5 / 7;
        background-color: rgba(255, 255, 255, 0.1);
        position: absolute;
        transition: transform 600ms cubic-bezier(.05, .43, .25, .95);
        background-size: cover;
    }
    .big_card {
        border-radius: 1vmin;
        top: 30%;

    }

    .little_card {
        width: 12vmin;
        aspect-ratio: 5 / 7;
        background-color: rgba(255, 255, 255, 0.1);
        border-radius: 2vmin;
        left: 45%;
        top: 45%
    }

    .big_card:nth-child(2) {
        background-color: aqua;
        background-image: url("https://images.pexels.com/photos/1458916/pexels-photo-1458916.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
        transform: translateX(-10%) rotate(-1deg);
    }

    .big_card:nth-child(4) {
        background-color: gold;
        background-image: url("https://images.pexels.com/photos/1390361/pexels-photo-1390361.jpeg");
        transform: rotate(2deg);
    }

    .big_card:nth-child(6) {
        background-color: green;
        background-image: url("https://images.pexels.com/photos/220938/pexels-photo-220938.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
        transform: translateX(-6%) rotate(-3deg);
    }

    .big_card:nth-child(8) {
        background-color: darkred;
        background-image: url("https://images.pexels.com/photos/1805164/pexels-photo-1805164.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
        transform: translate(10%, 3%) rotate(5deg);
    }
    .card_group:hover > .big_card:nth-child(2) {
        transform: translate(-80%, 10%) rotate(-30deg);
    }
    .card_group:hover > .big_card:nth-child(4) {
        transform: translate(-30%) rotate(-10deg);
    }
    .card_group:hover > .big_card:nth-child(6) {
        transform: translate(30%) rotate(10deg);
    }
    .card_group:hover > .big_card:nth-child(8) {
        transform: translate(80%, 10%) rotate(30deg);
    }

    .card_group:hover > .little_card:nth-child(1) {
        transform: translate(300%, 160%) rotate(10deg);
        background-image: url("https://images.pexels.com/photos/1170986/pexels-photo-1170986.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
    }
    .card_group:hover > .little_card:nth-child(3) {
        transform: translate(300%, -160%) rotate(-25deg);
        background-image: url("https://images.pexels.com/photos/2071882/pexels-photo-2071882.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
    }
    .card_group:hover > .little_card:nth-child(5) {
        transform: translate(-300%, 150%) rotate(-20deg);
        background-image: url("https://images.pexels.com/photos/2071881/pexels-photo-2071881.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
    }
    .card_group:hover > .little_card:nth-child(7) {
        transform: translate(-300%, -160%) rotate(20deg);
        background-image: url("https://images.pexels.com/photos/3777622/pexels-photo-3777622.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2");
    }
</style>