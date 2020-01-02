<template>
    <div class="header">
        <h3>Quotes Added</h3>
        <div class="progress">
            <div class="progress-bar" :style="{width:quoteCount/maxQuotes*100+ '%'}">
                {{quoteCount}} / {{maxQuotes}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:["quoteCount","maxQuotes"]
}
</script>

<style scoped>
.header {
    margin: 2rem 0 ;    
}

.progress{
    margin-top: 0.5rem;
    width: 100%;
    height: 2.5rem;
    background-color: #e7e7e7;
}

.progress-bar{
    height: 100%;
    background-color: aqua;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1rem;
    transition: all 0.6s ease;
}
</style>