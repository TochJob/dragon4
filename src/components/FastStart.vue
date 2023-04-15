<template>
    <div class="section">
        <h1 class="section__heading">Драгон Мани</h1>
        <p class="section__paragraph">Популярнейший игровой портал, позволяющий зарабатывать и выводить реальные деньги.</p>
        <div class="section__buttons">
     <button class="button" :class="item.option" v-for="(item, index) of sectionButtons" :key="index">{{ item.name }}</button>
        </div>
    </div>
</template>
<script>
export default {
    name: 'fastStart',
    data() {
        return {
            sectionButtons: [{
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
.section {
    background: #151B3D;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;

    &__heading {
        font-family: 'Raleway';
        font-style: normal;
        font-weight: 700;
        font-size: 40px;
        line-height: 47px;
        color: #FFFFFF;
        padding: 98px 0 27px 0;
    }

    &__paragraph {
        font-family: 'Raleway';
        font-style: normal;
        font-weight: 300;
        font-size: 15px;
        line-height: 22px;
        color: #FFFFFF;
    }
    
}
</style>