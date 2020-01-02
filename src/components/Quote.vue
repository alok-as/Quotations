<template>
    <div>
        <div class="quote">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    props:["quotes"]
}
</script>

<style scoped>

.quote{
    font-family: 'Arizonia', cursive;
    font-size: 25px;
    color: black;
    cursor: pointer;
    border: 2px solid #e6e6e6;
    padding: 1.2rem;
    text-align: center;
}

.quote:hover{
    background-color: #ffe2e2;
}
</style>