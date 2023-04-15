<template>
    <header class="header">
        <a class="header__link" href="">Dragon Money</a>
        <div class="header__buttons">
            <button class="button" :class="item.option" v-for="(item, index) of headerButtons" :key="index">{{ item.name }}
            </button>
        </div>
    </header>
</template>
<script>
export default {
    name: 'HeaderLanding',
    data() {
        return {
            headerButtons: [{
                name: 'Отзывы',
                option: ''
            },
            {
                name: 'Быстрый старт',
                option: ''
            },
            {
                name: 'Бонусы',
                option: ''
            }
            ]
        }
    }

}
</script>
<style lang="scss" scoped>
.header {
    background: linear-gradient(270deg, #FFB309 0%, #EEA849 100%);
    height: 50px;
    display: flex;
    justify-content: space-between;


    &__link {
        text-decoration: none;
        font-family: 'Arial';
        font-style: normal;
        font-weight: 400;
        font-size: 22px;
        line-height: 22px;
        color: #FFFFFF;
        margin: 12px 0 12px 14px;

    }

    &__buttons {
        display: flex;
        align-items: center;
        display: flex;
        gap: 27px;


        .button {
            font-family: 'Arial';
            font-style: normal;
            font-weight: 700;
            font-size: 14px;
            color: #220F09;  
            padding: 0 20px;     
            background: none; 
            border: none;
            cursor: pointer;
        }
    }
}
</style>