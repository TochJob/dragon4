<template>
  <section class="bonus">
    <HeaderSection title="Драгон Мани"
      desc="Драгон Мани — онлайн стратегия с уникальными играми! Краш, нвути, рулетка, дабл, монополия и другие игры! Ежедневные бонусы и праздничные события! Попробуй и получи бесплатный бонус 🔥 Официальный сайт" />
    <div class="wrapper bonus__wrapper">
      <a href="" class="button bonus__button">Регистрация</a>
      <div class="column info" v-for="(item, index) of infoList" :key="index">
        <h3 class="info__title">{{ item.title }}</h3>
        <p class="info__data">{{ item.data }}</p>
      </div>
    </div>
    <div class="column chapter">
      <h2 class="chapter__title">Дополнительные разделы</h2>
      <a href="" class="chapter__image">
        <img src="@/assets/img/chapter.png" alt="chapter" />
      </a>
    </div>
    <div class="column bonus__desc">
      <DescriptionBonus class="bonus__desc-item" v-for="(item, index) of descList" :key="index" :title="item.title"
        :text="item.text" />
    </div>
    <HelpSection />
    <a href="" class="button bonus__button bonus__reg">Получить 50 монет за регистрацию!</a>
    <h2 class="bonus__title">Обратите внимание</h2>
    <p class="bonus__text">Для получения бонусов необходимо</p>
    <BAttention class="bonus__attention" />
    <h2 class="bonus__title">Действующие бонусы</h2>
    <div class="wrapper bonus__coins">
      <div class="bonus__coins-item" v-for="(item, index) of coins" :key="index">
        <p class="bonus__text">{{ item.title }}</p>
        <p class="bonus__text">{{ item.desc }}</p>
      </div>
    </div>
    <BWeekly class="bonus__weekly" />
    <h2 class="bonus__title">Единоразовые</h2>
    <div class="column bonus__banners">
      <a href="" v-for="(item, index) of bannerImages" :key="index">
        <img :src="item.image" alt="banner" class="bonus__banners-image" />
      </a>
    </div>
    <h2 class="bonus__title">События</h2>
    <div class="wrapper bonus__events">
      <BEvent class="bonus__event" v-for="(item, index) of events" :key="index" :title="item.title" :text="item.text"
        :img="item.img" :coins="item.coins" :color="item.color" />
    </div>
    <h2 class="bonus__title">Реферальный бонус</h2>
    <BReferal />
  </section>
</template>
<script>
import HeaderSection from "@/components/HeaderSection.vue";
import HelpSection from "@/components/HelpSection.vue";
import DescriptionBonus from "@/components/DescriptionBonus.vue";
import BAttention from "@/components/Bonus/BAttention.vue";
import BWeekly from "@/components/Bonus/BWeekly.vue";
import BEvent from "@/components/Bonus/BEvent.vue";
import BReferal from "@/components/Bonus/BReferal.vue";

export default {
  components: {
    HeaderSection,
    DescriptionBonus,
    HelpSection,
    BAttention,
    BWeekly,
    BEvent,
    BReferal,
  },
  data() {
    return {
      infoList: [
        {
          title: "Игроков",
          data: "5,370,257",
        },
        {
          title: "Выплачено",
          data: "119,358,168,951",
        },
      ],
      descList: [
        {
          title: "Бонусы в казино Dragon Money",
          text: `Казино Драгон Мани постоянно обновляет свои акции, предлагая игрокам разнообразные бонусы: дополнительные средства, кэшбэк, фриспины или игровые монеты. Все эти Dragon Money бонусы предоставляются только зарегистрированным пользователям. Прежде чем воспользоваться бонусным предложением, необходимо изучить условия его получения и вейджер. Драгон Мани бонусы можно найти в разделе "Акции", а уже начисленные поощрения доступны в личном кабинете игрока.`,
        },
        {
          title: "Бонусы за регистрацию в Dragon Money",
          text: "При регистрации в казино Dragon Money игроки могут получить бонус, который состоит из дополнительных средств к депозиту и бесплатных вращений. Оба поощрения начисляются сразу после пополнения счета. Для быстрого получения реферальный бонус Dragon Money, рекомендуется верифицировать аккаунт.",
        },
        {
          title: "Бонус за первый депозит в Dragon Money",
          text: "Бонус на депозит в казино Драгон Мани составляет 100 или 125% – конкретный процент зависит от времени внесения депозита после регистрации. Если игрок внесет депозит в течение одного часа, к сумме депозита добавится 125%. В остальных случаях, к первому депозиту начисляется 100% бонуса. Максимальный размер бонуса в рамках данной акции составляет 20 000 руб.",
        },
        {
          title: "Бонус на депозит",
          text: "Бонус на депозит в казино Драгон Мани составляет 100 или 125% – конкретный процент зависит от времени внесения депозита после регистрации. Если игрок внесет депозит в течение одного часа, к сумме депозита добавится 125%. В остальных случаях, к первому депозиту начисляется 100% бонуса. Максимальный размер бонуса в рамках данной акции составляет 20 000 руб.",
        },
        {
          title: "250 FS за регистрацию в Dragon Money",
          text: [
            `При пополнении счета на сумму от 1000 руб и выше игрокам начисляются дополнительные 250 FS. Фриспины предоставляются частями: 50 вращений сразу после пополнения счета и по 40 фриспинов в течение 5 дней. Это поощрение можно получить только один раз.`,
            `Данный бонус активируется сразу после внесения депозита от 1000 руб. Фриспины доступны для использования в течение 48 часов. На отыгрыш бонусных средств предоставляется 24 часа после начисления, с вейджером х50. Статус отыгрыша можно отследить в личном кабинете пользователя.`,
          ],
        },
        {
          title: "Программа лояльности",
          text: [
            `Лояльностная программа казино Драгон Мани состоит из 9 уровней: от Новичка до Повелителя азарта. Первый уровень присваивается автоматически после регистрации. Переход между уровнями осуществляется при достижении игроком определенного количества монет. Монеты также известны как драгон-монеты. Заработанные монеты можно обменивать на бонусные деньги. После обмена, бонусные средства необходимо отыграть в соответствии с вейджером.`,
            `Задания, за которые начисляются промокоды драгон мани, делятся на два типа: базовые (заполнить профиль полностью, внести первый депозит, подтвердить email и т. д.) и ежедневные (сыграть в любом игровом автомате на реальные средства, прокрутить 5 разных слотов в течение дня и т. д.).`,
          ],
        },
        {
          title: "Где и как получить дополнительные промокоды",
          text: "Официальный сайт Dragon Money предоставляет каждому зарегистрированному пользователю возможность бесплатно получать игровую валюту. Промокоды Dragon Money – это комбинация символов, благодаря которым игрокам начисляются денежные бонусы. Размер вознаграждения определяется генератором случайных чисел.",
        },
      ],
      coins: [
        {
          title: "Получить 15 монет",
          desc: "15 монет можно получить 1 раз в день",
        },
        {
          title: "Получить 1 монету",
          desc: "1 монету можно получать каждые 5 минут с 10:00 до 0:00 по МСК",
        },
      ],
      bannerImages: [
        {
          image: require("@/assets/img/banners/tg.png"),
        },
        {
          image: require("@/assets/img/banners/vk.png"),
        },
      ],
      events: [
        {
          title: "День победы",
          text: "В честь великой победы дарим монеты",
          img: require("@/assets/img/banners/medal.png"),
          coins: "15",
          color: "#FFB309",
        },
        {
          title: "С началом лета!",
          text: "Дарим всем монеты по наступлению лета!",
          img: require("@/assets/img/banners/summer.png"),
          coins: "50",
          color: "rgba(58, 255, 9, 0.56)",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.bonus {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__attention {
    align-items: flex-end;
  }

  &__wrapper {
    align-items: center;
    gap: 60px;
    margin: 30px 0 52px;
  }

  &__button {
    font-family: "Arial";
    font-weight: 700;
    font-size: 14px;
    line-height: 40px;
    color: #220f09;
    background: #ffb309;
    border-radius: 8px;
    padding: 0 20px;
  }

  &__desc {
    margin: 40px 0;

    &-item {
      margin-bottom: 22px;
    }
  }

  &__title {
    align-self: flex-start;
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 31px;
    line-height: 37px;
    color: #ffffff;
  }

  &__reg {
    display: inline-block;
    margin: 40px 0;
  }

  &__text {
    font-family: "Montserrat";
    font-weight: 500;
    font-size: 16px;
    line-height: 37px;
    color: #ffffff;
    align-self: flex-start;
  }

  &__attention {
    margin: 15px 0 40px;
  }

  &__coins {
    margin: 6px 0 24px;
    width: 100%;
    justify-content: space-between;
  }

  &__weekly {
    margin-bottom: 46px;
  }

  &__banners {
    width: 100%;

    &-image {
      width: 100%;
    }
  }

  &__events {
    gap: 40px;
    align-self: flex-start;
    margin: 40px 0;
  }
}

.info {
  &__title {
    font-weight: 300;
    font-family: "Montserrat";
    font-size: 16px;
    line-height: 30px;
    color: #ffffff;
  }

  &__data {
    font-weight: 700;
    font-family: "Montserrat";
    font-size: 16px;
    line-height: 30px;
    color: #ffffff;
  }
}

.chapter {
  align-self: flex-start;

  &__title {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 24px;
    margin: 0 0 20px 50px;
    line-height: 30px;
    color: #ffffff;
    text-align: left;
  }
}

@media screen and (max-width: 1200px) {
  .chapter {
    &__image {
      img {
        width: 100%;
      }
    }
  }

  .bonus {
    &__events {
      flex-direction: column;
    }

    &__text {
      font-size: 13px;
      line-height: 240%;
    }
  }
}

@media screen and (max-width:576px) {
  .bonus {
    &__desc {
      margin-bottom: 20px;
    }

    &__text {
      line-height: 150%;
    }

    &__coins {
      &-item {
        display: flex;
        flex-direction: column;
        gap: 15px;
      }
    }
  }
}
@media screen and (max-width:480px) {
  .bonus{
    &__wrapper{
      flex-direction: column-reverse;
      gap: 10px;
      margin: 20px 0 ;
    }
    &__title{
      font-size: 16px;
      line-height: 150%;
    }
    &__reg{
      font-size: 11px;
      margin: 25px 0;
    }
    &__coins{
      flex-direction: column;
      gap: 25px;
      &-item{
        gap: 10px;
      }
    }
  }
  .chapter{
    &__title{
      margin-left: 0;
      font-size: 15px;
    }
  }
  .info{
    text-align: center;
    &__title{
      font-size: 13px;
    }
    &__data{
      font-size: 11px;
    }
  }
}
</style>
