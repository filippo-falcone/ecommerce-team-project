<script>
import RoundedCard from './RoundedCard.vue';

export default {
    components: {
        RoundedCard,
    },
    data() {
        return {
            data: [
                {
                    sectionTitle: 'Scopri i prodotti Made in Italy',
                    info: [
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Gifts_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Food_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Apparel_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Home_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Beauty_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Handmade_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Kitchen_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Deco_200x200._CB579229770_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/ACS/Made_in_Italy/2024/Gateways/04_April/MII_IT_BUBBLE_Toys_200x200._CB579229770_.jpg',
                        }
                    ]
                },
                {
                    sectionTitle: 'Scopri nuovi eccitanti prodotti',
                    info: [
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Favoritos_LR._CB559119013_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Deals_Bubble_LR._CB559119013_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Electronics_LR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Home_LR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Kitchen_LR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Fashion_HR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Sports_LR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Beauty_LR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_Food_LR._CB559113711_.jpg',
                        },
                        {
                            image: 'https://images-eu.ssl-images-amazon.com/images/G/29/Brand_Owners_B2C/2024/GATEWAY/APRIL/BUBBLE/IT_ToysBaby_LR._CB559113711_.jpg',
                        }
                    ]
                }
            ]
        };
    }
}
</script>

<template>
    <section>
        <div class="container">
            <div class="hstack gap-3 py-2">
                <h3 class="mb-0">{{ data[0].sectionTitle }}</h3>
                <a href="#">Scopri</a>
            </div>
            <div class="hstack gap-2  overflow-x-hidden">
                <RoundedCard v-for="info in data[0].info" :cardInfo="info"></RoundedCard>
            </div>
            <div class="arrow left">
                <i class="fa-solid fa-chevron-left fa-2xl"></i>
            </div>
            <div class="arrow right">
                <i class="fa-solid fa-chevron-right fa-2xl"></i>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

section {
    .container {
        background-color: $brand_light;
    }
}
</style>