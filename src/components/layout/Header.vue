<template>
  <header class="header">
    <a class="header__link" href="">Dragon Money</a>
    <div class="header__buttons">
      <router-link 
        :to="item.to"
        class="button"
        v-for="(item, index) of headerButtons"
        :key="index"
      >
        {{ item.name }}
      </router-link>
    </div>
    <div class=""></div>
  </header>
</template>
<script>
export default {
  name: "HeaderLanding",
  data() {
    return {
      headerButtons: [
        {
          name: "Отзывы",
          to: "/reviews",
        },
        {
          name: "Быстрый старт",
          to: "/",
        },
        {
          name: "Бонусы",
          to: "/bonus",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.header {
  background: linear-gradient(270deg, #ffb309 0%, #eea849 100%);
  height: 50px;
  display: flex;
  justify-content: space-between;

  &__link {
    text-decoration: none;
    font-family: "Arial";
    font-style: normal;
    font-weight: 400;
    font-size: 22px;
    line-height: 22px;
    color: #ffffff;
    margin: 12px 0 12px 14px;
  }

  &__buttons {
    display: flex;
    align-items: center;
    display: flex;
    gap: 27px;
    text-align: center;

    .button {
      font-family: "Arial";
      font-style: normal;
      font-weight: 700;
      font-size: 14px;
      color: #220f09;
      padding: 0 20px;
      background: none;
      border: none;
      
    }
  }
}
</style>
