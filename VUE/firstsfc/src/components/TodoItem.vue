<template>
    <div class="pinkBall"></div>
    <li v-bind="$attrs"> {{ itemName }}  </li>
    <div class="pinkBall"></div>
</template>

<script>
    export default {
        props: ['itemName']
    }
</script>

<style>
    .pinkBall {
        display: inline-block;
        margin: 2px;
        padding: 5px;
        background-color: lightpink;
        border-radius: 50%;
    }
    li {
        margin: 0;
        padding: 5px 10px;
        border-radius: 10px;
    }
</style>