<template>
    <div id="product-inventory">
        <h2>{{ product }} are in stock.</h2>
    </div>
</template>

<script>
export default {
    name: "ProductInventory",
    data: () => {
        return {
            product: "Boots"
        };
    }
}
</script>

<style scoped>
#product-inventory {
    text-align: center;
}
</style>