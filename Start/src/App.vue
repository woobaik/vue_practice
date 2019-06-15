<template>
    <div class="container">
        <app-new-quote @quoteIsAdded="addQuote" ></app-new-quote>        
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    </div>
</template>

<script>
    import quoteGrid from './components/QuoteGrid.vue'
    import newQuote from './components/NewQuote.vue'
    export default {
        data: function() {
            return {
                quotes: ['THis is a sample quote'],
                maxQUotes: 10
            }
        },
        methods: {
            addQuote(quote) {
                this.quotes.push(quote)
             
            },
            deleteQuote(index) {
                this.quotes.splice(index,1)
            }
        },
        components: {
            AppQuoteGrid: quoteGrid,
            AppNewQuote: newQuote
        }
    }
</script>

<style>
</style>
