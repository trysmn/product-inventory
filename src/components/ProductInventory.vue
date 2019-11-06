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
            products: [
                "Boots",
                "Jacket",
                "Hiking Socks"
            ]
        };
    }
}
</script>

<style scoped>
#product-inventory {
    text-align: center;
    list-style-position: inside;
}
</style>