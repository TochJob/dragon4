<template lang="">
  <div class="help">
    <p class="help__text">Существует несколько способов получения промокодов драгон мани:</p>
    <ol class="help__list">
      <li class="help__list-item" v-for="(item, index) of helpList" :key="index">
        <p class="help__text">{{ item }}</p>
      </li>
    </ol>
    <p class="help__text">Для активации промокода необходимо выполнить следующие шаги:</p>
    <ol class="help__list">
      <li class="help__list-item" v-for="(item, index) of activateList" :key="index">
        <p class="help__text">{{ item }}</p>
      </li>
    </ol>
    <p class="help__text">Игровые монеты будут зачислены на счет мгновенно.</p>
  </div>
</template>
<script>
export default {
  name: "HelpSection",
  data() {
    return {
      helpList: [
        "В официальной группе ВКонтакте. Администрация сообщества регулярно проводит конкурсы репостов и определяет победителей с помощью сервиса Random.org.",
        "В Телеграм-чате. Модераторы публикуют промокоды с различным номиналом в течение дня.",
        "На тематических форумах и сайтах. Игроки часто предоставляют реферальные промокоды драгон мани, которые позволяют новичкам получить 50 бонусных монет при регистрации.",
        "На ютуб-каналах блогеров. Промокоды можно найти в комментариях к видеообзорам. Там же указывают ссылку на официальный сайт.",
      ],
      activateList: [
        "Авторизуйтесь на официальном сайте Драгон Мани.",
        'Перейдите в раздел "Бонусы".',
        "Введите код (например, DRGNMBLOG) в специальное поле.",
        'Нажмите "Активировать".',
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.help {
  width: 90%;
  align-self: flex-start;
  &__text {
    font-family: "Montserrat";
    font-weight: 300;
    font-size: 16px;
    line-height: 27px;
    color: #ffffffbd;
  }
  &__list {
    margin: 30px 0;
    color: #ffffffbd;
  }
}
</style>
