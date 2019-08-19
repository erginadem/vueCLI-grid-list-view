<template>
    <div class="product-list">
        <div class="text-right">
            <a href="#" class="nav-link-inline" @click="changeView('list')">List</a> |
            <a href="#" class="nav-link-inline" @click="changeView('grid')">Grid</a>
            <hr />
        </div>
        <div class="products" :class="{'grid' : gridView}">
            <product
                class="text text-secondary mt-2"
                v-for="product in products"
                :name="product.name"
                :price="product.price"
                :key="product.id"
                >
                {{ product.description }}
            </product>
        </div>
    </div>
</template>

<script>
    import Product from './Product.vue'

    export default {
        components: { Product },

        methods: {
            changeView(type) {
                if (type == 'grid') {
                    this.gridView = true;
                } else {
                    this.gridView = false;
                }
            }

        },

        data() {
            return {

                gridView: false,

                products: [
                    {
                        id: 1,
                        name: 'LAMP',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                        price: 19.9
                    },

                    {
                        id: 2,
                        name: 'TABLE',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                        price: 89.9
                    },

                    {
                        id: 3,
                        name: 'TV',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                        price: 999.9
                    },

                    {
                        id: 4,
                        name: 'MIRROR',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                        price: 9.9
                    },

                    {
                        id: 5,
                        name: 'GLASS',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                        price: 2.9
                    },

                    {
                        id: 6,
                        name: 'HAIR DRYER',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
                        price: 59.9
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .products {
        display: flex;
        flex-direction: column;
    }

    .grid {
        flex-direction: row;
        flex-wrap: wrap;

        .product {
            flex-basis: 15%;
        }
    }
</style>
