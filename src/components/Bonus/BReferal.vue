<template>
  <div class="referal wrapper">
    <img src="@/assets/img/banners/chest.png" alt="chest" />
    <div class="referal__box">
      <h4 class="referal__title">Вас пригласили? Есть промокод?</h4>
      <p class="referal__text">Получайте монеты бесплатно, за один промокод минимум 50 монет!</p>
      <div class="referal__form">
        <input type="text" class="referal__input" placeholder="Промокод" />
        <AutorisationButton/>
      </div>
    </div>
  </div>
</template>
<script>
import AutorisationButton from '@/components/UI/AutorisationButton.vue'
export default {
  components:{
    AutorisationButton
  }
};
</script>
<style lang="scss" scoped>
.referal {
  align-items: center;
  margin-top: 15px;
  &__box {
  }
  &__title {
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 31px;
    line-height: 37px;
    color: #ffffff;
  }
  &__text {
    font-family: "Montserrat";
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    color: #ffffff;
  }
  &__form {
    margin-top: 20px;
  }
  &__input {
    border: 1px solid #ffffff;
    filter: drop-shadow(0px 2px 30px rgba(0, 0, 0, 0.2));
    min-width: 273px;
    border-radius: 7px;
    padding: 10px;
    color: #fff;
    background: transparent;
    margin-right: 28px;
    &::placeholder {
      color: rgba(255, 255, 255, 0.6);
    }
  }
  &__button {
    
  }
}
</style>
