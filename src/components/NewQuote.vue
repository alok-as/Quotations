<template>
    <form class="add-quote">
        <label>Quote</label>
        <textarea rows="3" v-model="quote"></textarea>
        <button @click.prevent="createNew">Add Quote</button>
    </form>
</template>

<script>

export default {
    data(){
        return {
            quote:""
        }
    },
    methods:{
        createNew:function(){
            this.$emit("quoteAdded",this.quote);
            this.quote="";
        }
    }
}
</script>

<style scoped>
.add-quote{
    width: 50%;
    margin: 0 auto;
    margin-bottom: 4rem;
}

.add-quote label{
    display: block;
    font-weight: bold;
    margin-bottom: 0.5rem;
}
.add-quote textarea{
    width: 100%;
    margin-bottom: 0.5rem;
    /* outline: none; */
    border: 1px solid #555;
    padding: 0.5rem;
    font-size: 1.2rem;

}

.add-quote button {
    display:block;
    background-color:aqua;
    color: black;
    border: none;
    outline: none;
    border-radius: 5px;
    padding: 0.6rem 2rem;
    cursor: pointer;
    font-family: 'Poppins', sans-serif;
    transition: all 0.6s ease-in;

}


/* No Challenges No Success,Know Challenges Know Success. */

</style>