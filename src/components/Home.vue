<template>
    <div class="home">        
        <SearchHome></SearchHome>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';
    import SearchHome from './../components/SearchHome.vue'

    @Component({
        components: {
            SearchHome
        }
    })
    export default class Home extends Vue {
        @Prop() private msg!: string;
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
