<template>
  <section class="reviews">
    <HeaderSection
      title="Драгон Мани"
      desc="Драгон Мани 🐉 — онлайн стратегия с уникальными играми! Краш, нвути, рулетка, дабл, монополия и другие игры! Ежедневные бонусы и праздничные события! Попробуй и получи бесплатный бонус 🔥 Официальный сайт"
    />
    <div class="banner wrapper">
      <div class="banner__box">
        <h2 class="banner__title">Оставить отзыв</h2>
        <p class="banner__subtitle">
          Вы можете оставить отзыв о драгонмани в группе вконтакте или же прямо на сайте
        </p>
        <div class="wrapper banner__datas">
          <p class="banner__data" v-for="(item, index) of bannersData" :key="index">
            <span>{{ item.count }}</span
            >{{ item.title }}
          </p>
        </div>
      </div>
      <div class="wrapper banner__buttons">
        <a
          href=""
          v-for="(item, index) of bannersButtons"
          :key="index"
          class="banner__button"
          :class="item.class"
        >
          <img v-if="item.svg" :src="item.svg" alt="button" />
          {{ item.title }}
        </a>
      </div>
    </div>

    <div class="description">
      <p class="description__text">
        <a href="">Отзывы об онлайн-казино Драгон Мани</a> приходят от самых разных игроков, и
        каждый имеет свое мнение об этой платформе. Прочитайте отзывы о казино
        <a href="">Драгон Мани</a> от реальных игроков, узнайте, стоит ли доверять данному
        онлайн-казино, какие преимущества и недостатки есть у игровой платформы.
      </p>
      <p class="description__text">
        Согласно <a href="">драгон мани отзывы</a> игроков, одним из основных преимуществ казино
        является большой выбор игр от популярных разработчиков. Это привлекает множество игроков,
        которые ищут новые развлечения и хотят попробовать удачу в разнообразных игровых автоматах.
      </p>
      <p class="description__text">
        <a href=""> Dragon money отзывы</a> также подчеркивают, что казино активно развивает свою
        бонусную программу, предлагая разнообразные промокоды и акции. Это позволяет пользователям
        получать дополнительные вознаграждения и увеличивать свои шансы на выигрыш.
      </p>
      <p class="description__text">
        Некоторые <a href="">dragon money casino отзывы</a> указывают на то, что платформа
        обеспечивает надежную систему безопасности, сохраняя данные пользователей в тайне и
        предотвращая возможные мошеннические действия. Кроме того, игроки отмечают, что служба
        поддержки казино оперативно решает возникающие вопросы и помогает в случае возникновения
        проблем.
      </p>
      <p class="description__text">
        Однако, в <a href="">драгон мани отзывы реальные</a> можно встретить и критические
        замечания. Некоторые игроки жалуются на долгую верификацию аккаунта и задержки при выводе
        средств. В то же время, другие утверждают, что их опыт работы с казино был положительным и
        они смогли быстро снять свои выигрыши.
      </p>
      <p class="description__text">
        В целом, онлайн-казино <a href="">Драгон Мани</a> представляется как достойное онлайн-казино
        с широким выбором игр, привлекательной бонусной программой и надежной системой безопасности.
        Однако, прежде чем начать играть, каждый пользователь должен оценить имеющиеся отзывы и
        сделать собственные выводы, учитывая свои предпочтения и опыт игры в онлайн-казино.
      </p>
      <p class="description__text">
        В следующем разделе мы представляем вашему вниманию подборку
        <a href="">реальных отзывов от игроков </a> о казино Драгон Мани. Эти мнения были собраны с
        различных ресурсов, таких как форумы, социальные сети и блоги, чтобы дать вам максимально
        полное и объективное представление о качестве игровой платформы. Отзывы этих пользователей
        отражают их личный опыт и могут быть полезными при принятии решения о том, стоит ли вам
        играть на этом сайте. Мы приглашаем вас внимательно изучить представленные мнения и сделать
        собственные выводы, учитывая свои предпочтения и ожидания от онлайн-казино.
      </p>
    </div>

    <div class="reviews__block">
      <div class="review wrapper" v-for="(item, index) of revierws" :key="index">
        <img :src="item.sex" alt="preson" />
        <div class="review__info">
          <h3 class="review__name">{{ item.title }}</h3>
          <p class="review__text">{{ item.text }}</p>
        </div>
        <p class="review__date">{{ item.date }}</p>
      </div>
    </div>
    <a href="" class="button">Написать отзыв</a>
  </section>
</template>
<script>
import HeaderSection from "@/components/HeaderSection.vue";

export default {
  components: {
    HeaderSection,
  },
  data() {
    return {
      bannersData: [
        {
          title: "на основе",
          count: "4,96/5",
        },
        {
          title: "отзывов",
          count: "558",
        },
      ],
      bannersButtons: [
        {
          title: "Написать",
          svg: "",
          class: "",
        },
        {
          title: "Вконтакте",
          svg: require("@/assets/img/media/vk.svg"),
          class: "vk",
        },
      ],
      revierws: [
        {
          title: "Алексей",
          text: "Ого, ну это крутое казино! В Драгон Мани кайф играть, особенно в слоты. Бонусы приятные, быстро выводят деньги. Рекомендую!",
          date: "15.01.2023",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "LuckyStar21 ",
          text: "Это жесть, какое казино! Реально крутые автоматы, а бонусы - просто класс. Вывод денег быстрый, поддержка адекватная. Заходите, не пожалеете!",
          date: "27.01.2023",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "FortuneHunter",
          text: "Привет всем азартным друзьям! Скажу вам, здесь просто шик! Игры, бонусы, вывод денег - всё просто супер. Обожаю это казино!!!",
          date: "15.01.2023",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "AdventureSeeker",
          text: "Неплохое казино, но могло бы быть лучше. Игры в целом интересные, но я бы хотел видеть больше разнообразия. Бонусы тоже неплохие, но иногда их сложно отыграть. Вывод денег работает быстро, это радует. В целом, сойдет.",
          date: "21.03.2023",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "Игорь",
          text: "Скептически относился к онлайн-казино, но Драгон Мани полностью изменило мое мнение. Удобно, безопасно и развлекательно.",
          date: "14.11.2022",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "CrazyGambler88",
          text: "Братаны, это же рай для азартных людей! Здесь всё круто, игры, бонусы, вывод бабла. Не раз уже выигрывал, всё честно. ",
          date: "09.01.2023",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "Паша  ",
          text: "В принципе, казино хорошее, но есть куда стремиться. Хотелось бы больше акций и бонусов для постоянных игроков. Иногда поддержка медленно отвечает, но в итоге все решается. Игры интересные, вывод денег быстрый, так что в целом я доволен.",
          date: "02.09.2022",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "SunnyDaze",
          text: "Оставляю свой отзыв о казино: играю уже год, всегда только положительные эмоции. Рекомендую попробовать!",
          date: "02.07.2022",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "MoskvaCity2022",
          text: "Привет всем азартным друзьям!:) Скажу вам, здесь просто шик! Игры, бонусы, вывод денег - всё просто супер. Обожаю это казино!",
          date: "24.04.2022",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "VadimKolesnikov91",
          text: "Играю уже некоторое время, все неплохо, но дизайн сайта мог бы быть получше. В остальном, все ок!",
          date: "30.11.2022",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "DaryaSokolova995",
          text: "Драгон Мани - хорошее казино, но иногда проблемы с техподдержкой. Тем не менее, в целом довольна. Вывод средств работает исправно, но думаю, мобильная версия могла бы быть лучше оптимизирована.",
          date: "11.02.2023",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "AlexeyS_999",
          text: "Играю в Драгон Мани около двух лет, и в целом казино хорошее. Есть широкий выбор игр, и даже видеопокер! Но есть один недостаток - служба поддержки не всегда отвечает оперативно, особенно в выходные. Было бы неплохо, если бы они улучшили этот аспект",
          date: "08.05.2022",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "Lera_Starzzz",
          text: "Я прям влюбилась в Драгон Мани! Они типа даже дали мне бонусы за регистрацию, и я просто начала выигрывать! У них там куча крутых слотов, и даже моя мама играет теперь. Лучшее казино, серьезно!",
          date: "09.12.2022",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "Nastya_Cool_03",
          text: "Омг, ребята, этот Драгон Мани просто топ! Насмотрелась на мемасы в инсте и решила попробовать поиграть. Какой кайф выигрывать, я вам скажу! И вообще, атмосфера казино такая крутая, сразу чувствуешь себя как настоящий гемблер))) Рекомендую всем друзьям!",
          date: "10.12.2022",
          sex: require("@/assets/img/persons/woman.png"),
        },
        {
          title: "IvanFFFedorov60",
          text: `Я довольно давно играю в казино Драгон Мани, и могу сказать, что это хорошее место для развлечения. Отличный выбор игр и быстрая обработка выплат. Но есть одно "но" - хотелось бы, чтобы в казино были доступны более удобные фильтры для поиска и сортировки игр, так как сейчас иногда бывает сложно найти нужный слот. В остальном, все отлично.`,
          date: "20.02.2023",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "Dima_Legend01",
          text: "Эй, братаны, вы только проверьте это казино Драгон Мани! Игры просто огонь, а когда выигрываешь - это такой адреналин! Они мне еще фриспины дали, и я реально выиграл! Не проходите мимо, это стоит того!",
          date: "07.03.2023",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "ash8888_22",
          text: "Чуваки, я просто в восторге от Драгон Мани!!! Такое крутое казино, они даже дали мне бонусы за регистрацию! Игры просто супер, и я уже выиграл несколько раз. Это просто огонь, ребята! Всем советую!",
          date: "17.08.2021",
          sex: require("@/assets/img/persons/man.png"),
        },
        {
          title: "Roma_WinKing",
          text: "Эй, все, кто любит азарт, Драгон Мани - это ваш выбор! Я там поиграл и не могу оторваться, слоты просто классные! Уже выиграл несколько раз и планирую еще больше! Ставлю этому казино 5 звезд!",
          date: "02.06.2022",
          sex: require("@/assets/img/persons/man.png"),
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.reviews {
  display: flex;
  flex-direction: column;
  .banner {
    border: 1px solid #ffffff;
    align-items: center;
    margin: 110px 0 40px;
    filter: drop-shadow(0px 2px 30px rgba(0, 0, 0, 0.2));
    border-radius: 30px;
    background-image: url("@/assets/img/banners/stiks.png");
    background-repeat: no-repeat;
    background-position: bottom left;
    padding: 40px 22px 35px 400px;
    &__title {
      font-weight: 700;
      font-size: 28px;
      line-height: 34px;
      color: #ffffff;
      max-width: 216px;
    }
    &__subtitle {
      font-weight: 600;
      font-size: 16px;
      line-height: 19px;
      color: #ffffff;
      margin: 20px 0 25px;
      max-width: 340px;
    }
    &__datas {
      gap: 7px;
      align-items: center;
    }
    &__data {
      font-weight: 600;
      font-size: 23px;
      line-height: 28px;
      color: #ffffff;
      span {
        font-family: "Exo";
        font-weight: 700;
        font-size: 32px;
        line-height: 38px;
        margin-right: 7px;
        color: #ffb400;
      }
    }

    &__buttons {
      gap: 20px;
    }

    &__button {
      font-weight: 600;
      font-size: 18px;
      line-height: 28px;
      display: flex;
      text-decoration: none;
      align-items: center;
      border-radius: 5px;
      border: none;
      padding: 10px 15px;
      color: #000;
      background: #ffb400;
      img {
        margin-right: 8px;
      }
      &.vk {
        color: #fff;
        background: #369bf9;
      }
    }
  }
  .description {
    display: flex;
    flex-direction: column;
    gap: 25px;
    &__text {
      font-family: "Montserrat";
      font-weight: 500;
      font-size: 16px;
      line-height: 27px;
      color: #ffffff85;
      a {
        font-weight: 700;
        text-decoration: none;
        color: #ffffff;
      }
    }
  }

  &__block {
    display: flex;
    flex-wrap: wrap;
    gap: 36px;
    justify-content: space-between;
    margin: 36px 0 60px;
  }

  .review {
    display: flex;
    align-items: flex-start;
    position: relative;
    border: 0.5px solid #ffffff;
    border-radius: 10px;
    gap: 20px;
    flex: 0 1 47%;
    padding: 12px 18px 25px 12px;
    &__info {
      display: flex;
      flex-direction: column;
    }
    &__name {
      font-family: "Montserrat";
      font-weight: 600;
      font-size: 16px;
      line-height: 27px;
      color: #ffffff;
      margin-bottom: 8px;
    }
    &__text {
      font-family: "Montserrat";
      font-weight: 300;
      font-size: 16px;
      line-height: 27px;
      color: #ffffffc5;
    }
    &__date {
      font-family: "Montserrat";
      font-weight: 300;
      font-size: 16px;
      line-height: 27px;
      color: #ffffffc5;

      position: absolute;
      top: 12px;
      right: 12px;
    }
  }
  .button {
    font-weight: 600;
    font-size: 18px;
    line-height: 28px;
    color: #000000;
    background: #ffb400;
    border-radius: 5px;
    padding: 24px 97px;
    align-self: center;
  }
}

@media screen and (max-width: 1200px) {
  .reviews {
    .banner {
      background-size: 25%;
      padding-left: 239px;
    }
  }
}
@media screen and (max-width: 992px) {
  .reviews {
    .banner {
      background-image: none;
      padding-left: 20px;
    }
  }
}
@media screen and (max-width: 768px) {
  .reviews {
    .banner {
      flex-direction: column;
      align-items: flex-start;
      gap: 10px;
    }
    .review {
      flex: 0 1 46%;
      gap: 10px;
      padding: 10px;
      img {
        width: 30px;
      }
      &__name {
        font-size: 11px;
      }
      &__text {
        font-size: 9px;
        line-height: 150%;
      }
      &__date {
        font-size: 10px;
      }
    }
    &__block {
      margin: 20px 0;
    }
    .button {
      font-size: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      padding: 10px;
    }
    .description {
      &__text {
        font-size: 11px;
        line-height: 150%;
      }
    }
    .banner {
      padding: 15px;
      margin: 30px 0;
      &__title {
        font-size: 13px;
      }
      &__subtitle {
        font-size: 11px;
        margin: 10px 0 10px;
      }
      &__data {
        font-size: 11px;
        span {
          font-size: 13px;
        }
      }
      &__button {
        padding: 0 15px;
        font-size: 11px;
        img {
          width: 15px;
          margin-right: 5px;
        }
      }
    }
  }
}
@media screen and (max-width: 480px) {
  .reviews {
    &__block{
      gap: 15px;
    }
    .review {
      flex: 0 1 auto;
    }
  }
}
</style>
