<template>
  <div class="attention wrapper">
    <div class="attention__item" v-for="(item, index) of list" :key="index">
      <p class="attention__title">{{ item.title }}</p>
      <a href="">
        <img :src="item.image" :alt="item.title" />
      </a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: [
        {
          title: "Вступить в группу Вконтакте",
          image: require("@/assets/img/socials/vk.png"),
        },
        {
          title: "Вступить в канал Telegram",
          image: require("@/assets/img/socials/tg.png"),
        },
        {
          title: "Привязать аккаунт телеграмма",
          image: require("@/assets/img/socials/bot.png"),
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.attention {
  border: 1px solid #ffffff;
  filter: drop-shadow(0px 2px 30px rgba(0, 0, 0, 0.2));
  border-radius: 30px;
  width: 100%;
  display: flex;
  justify-content: space-around;
  padding: 20px 0;

  &__item {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  &__title {
    font-family: "Montserrat";
    font-weight: 500;
    font-size: 16px;
    line-height: 37px;
    text-align: center;
    color: #ffffff;
  }
}


@media screen and (max-width:992px) {
  .attention{
    &__title{
      font-size: 11px;
      line-height: auto;
    }
    &__item{
      display: flex;
      flex-direction: column;
      align-items: center;
      img{
        width: 80%;
      }
      a{
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
  }
}

@media screen and (max-width:768px) {
  .attention{
    &__title{
      font-size: 9px;
      line-height: 150%;
      margin-bottom: 10px;  
    }
   
  }
}
</style>
