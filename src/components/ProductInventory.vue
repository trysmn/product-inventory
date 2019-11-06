<template>
    <div id="product-inventory">
        <ul>
            <li v-bind:key="product" v-for="product in products">
                {{ product }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'ProductInventory',
    data: () => {
        return {
            products: []
        };
    },
    created() {
        fetch('https://api.myjson.com/bins/74l63')
            .then(response => response.json())
            .then(json => {
                this.products = json.products;
            })
    }
}
</script>

<style scoped>
#product-inventory {
    text-align: center;
    list-style-position: inside;
}
</style>