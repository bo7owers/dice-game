<script setup lang="ts">
// For each dot that appears, add custom class of .pos-top-1
</script>
<template>
    <div class="container die-cont">
        <div class="die">
            <div class="dot pos-top-1"></div>
            <div class="dot pos-top-3"></div>
            <div class="dot pos-mid-1"></div>
            <div class="dot pos-mid-3"></div>
            <div class="dot pos-bot-1"></div>
            <div class="dot pos-bot-3"></div>
        </div>
    </div>
</template>
<style scoped>
.die {
    width: 80px;
    height: 80px;
    margin: 5px;
    border-radius: 12px;
    box-shadow: 0 0 10px rgb(0 0 0.25);

    display: grid;
    grid-template-columns: 2fr 0.25fr 2fr;
    grid-template-rows: 1fr 0.5fr 1fr;
    grid-template-areas:
        'top-1 top-2 top-3'
        'mid-1 mid-2 mid-3'
        'bot-1 bot-2 bot-3';
    justify-items: center;
}

.dot {
    width: 15px;
    height: 15px;
    background-color: #333;
    border-radius: 50%;
    align-self: center;
}

.dot.pos-top-1 {
    grid-area: top-1;
}

.dot.pos-top-3 {
    grid-area: top-3;
}
.dot.pos-mid-1 {
    grid-area: mid-1;
}

.dot.pos-mid-3 {
    grid-area: mid-3;
}
.dot.pos-bot-1 {
    grid-area: bot-1;
}
.dot.pos-bot-2 {
    grid-area: bot-2;
}

.dot.pos-bot-3 {
    grid-area: bot-3;
}
</style>
