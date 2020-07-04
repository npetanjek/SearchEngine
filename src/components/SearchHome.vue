<template>
    <div class="search-home">
        <div class="search-bar">
            <div class="search-header">
                <div class="search-title">{{ searchTitle }}</div>
            </div>
            <div class="search-content">
                <input class="search-input" v-model="searchInput" :placeholder="searchPlaceholder" />
                <div class="search-button material-icons" @click="onSearchClick()">
                    search
                </div>
                <div v-if="searchInput.length > 0" class="search-clear material-icons" @click="clearSearchInput()">
                    clear
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component({
        components: {

        }
    })
    export default class SearchHome extends Vue {
        searchTitle: String = 'MySearchEngine'
        searchPlaceholder: String = 'Insert your search phrase here...';
        searchInput: String = '';

        onSearchClick() {
            console.log(this.searchInput);
        }

        clearSearchInput() {
            this.searchInput = '';
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    .search-home {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100vh;
    }

    .search-bar {
        display: flex;
        flex-direction: column;
    }

    .search-content {
        display: flex;
        position: relative;
    }

    .search-header {
        margin-bottom: 24px;
        color: cornflowerblue;
    }

    .search-title {
        font-size: 38px;
        font-family: cursive;
    }

    .search-input {
        border: solid 1px gray;
        width: 500px;
        padding: 24px;
    }

    .search-button {
        width: 65px;
        height: 65px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: cornflowerblue;
        color: white;
        font-size: 28px;
    }

        .search-button:hover {
            cursor: pointer;
            background: lightskyblue;
        }

    .search-clear {
        position: absolute;
        right: 80px;
        top: 20px;
        color: gray;
    }

        .search-clear:hover {
            cursor: pointer;
            color: lightskyblue;
        }
</style>
