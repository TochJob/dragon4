<template>
  <section class="section">
    <HeaderSection
      title="Драгон Мани"
      desc="Драгон Мани — онлайн стратегия с уникальными играми! Краш, нвути, рулетка, дабл, монополия и другие игры! Ежедневные бонусы и праздничные события! Попробуй и получи бесплатный бонус 🔥 Официальный сайт"
    />
    <div class="section__games">
      <h2 class="section__name">Игры</h2>
      <Games />
    </div>
  </section>
</template>

<script>
import Games from "@/components/Games.vue";
import HeaderSection from "@/components/HeaderSection.vue";

export default {
  name: "HomeLand",
  components: {
    Games,
    HeaderSection
  },
  data() {
    return {
      sectionButtons: [
        {
          name: "Отзывы",
          option: "/reviews",
        },
        {
          name: "Быстрый старт",
          option: "/",
        },
        {
          name: "Бонусы",
          option: "/bonus",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;

  &__heading {
    font-style: normal;
    font-weight: 700;
    font-size: 40px;
    line-height: 47px;
    color: #ffffff;
    padding: 98px 0 27px 0;
  }

  &__paragraph {
    font-style: normal;
    font-weight: 300;
    font-size: 15px;
    line-height: 22px;
    color: #ffffff;
  }

  &__buttons {
    display: flex;
    align-items: center;
    display: flex;
    gap: 27px;
    padding: 28px 0 78px 0;

    .button {
      background: #ffb309;
      border-radius: 8px;
      font-family: "Arial";
      font-style: normal;
      font-weight: 700;
      font-size: 14px;
      line-height: 40px;
      color: #220f09;
      cursor: pointer;
      padding: 0 20px;
    }
  }

  &__name {
    font-family: "Raleway";
    font-style: normal;
    font-weight: 700;
    font-size: 30px;
    line-height: 35px;
    color: #ffffff;
    padding: 22px 0 30px 0;
  }

  &__games {
    border: 0.5px solid #ffffff;
    border-radius: 10px;
    display: flex;
    align-items: center;
    flex-direction: column;
    box-sizing: border-box;
    padding: 22px 85px 40px 85px;
    margin-top: 20px;
  }
}

@media screen and (max-width: 576px) {
  .section{
    &__games{
      padding: 15px 30px;
    }
  }
}
@media screen and (max-width: 480px) {
  .section{
    &__name{
      font-size: 15px;
      padding: 10px 0;
    }
    &__games{
      margin-top: 10px;
      padding: 5px 10px;
    }
  }
}
</style>
