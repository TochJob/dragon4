<template>
  <section class="section">
    <h1 class="section__heading">Драгон Мани</h1>
    <p class="section__paragraph">Популярнейший игровой портал, позволяющий зарабатывать и выводить реальные деньги.</p>
    <div class="section__buttons">
      <button class="button" :class="item.option" v-for="(item, index) of sectionButtons" :key="index">{{ item.name
      }}</button>
    </div>
    <div class="section__games">
      <h2 class="section__name">Игры</h2>
      <Games />
    </div>
    <Footer/>
  </section>
</template>

<script>
import Games from '@/components/Games.vue';
import Footer from '@/components/Footer.vue'

export default {
  name: 'HomeLand',
  components: {
    Games,
    Footer
  },
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
  },

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

  &__buttons {
    display: flex;
    align-items: center;
    display: flex;
    gap: 27px;
    padding: 28px 0 78px 0;


    .button {
      background: #FFB309;
      border-radius: 8px;
      font-family: 'Arial';
      font-style: normal;
      font-weight: 700;
      font-size: 14px;
      line-height: 40px;
      color: #220F09;
      cursor: pointer;
      padding: 0 20px;
    }
  }

  &__name {
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 700;
    font-size: 30px;
    line-height: 35px;
    color: #FFFFFF;
    padding: 22px 0 30px 0;
  }

  &__games {
    border: 0.5px solid #FFFFFF;
    border-radius: 10px;
    display: flex;
    align-items: center;
    flex-direction: column;
    box-sizing: border-box;
    width: 1080px;
    height: 444px;
    padding: 0 85px;
  }
}
</style>