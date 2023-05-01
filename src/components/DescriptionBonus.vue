<template>
  <div class="description">
    <h4 class="description__title">{{ title }}</h4>
    <template v-if="typeof(text) == 'object'">
      <p class="description__text" v-for="(item, index) of text" :key="index">{{ item }}</p>
    </template>
    <template v-else>
      <p class="description__text">{{ text }}</p>
    </template>
  </div>
</template>
<script>
export default {
  name: "DescriptionBonus",
  props: ["title", "text"],
};
</script>
<style lang="scss" scoped>
.description {
  &__title {
    font-family: "Montserrat";
    font-weight: 700;
    font-size: 39px;
    line-height: 43px;
    color: #ffffff;
    margin-bottom: 12px;
  }
  &__text {
    font-family: "Montserrat";
    font-weight: 300;
    font-size: 16px;
    line-height: 27px;
    text-indent: 5.68434e-14px;
    color: #ffffff96;
  }
}

@media screen and (max-width:576px) {
  .description{
    &__title{
      font-size: 16px;
      margin-bottom: 0; 
    }
    &__text{
      font-size: 11px;
      line-height: 150%;
    }
  }
}
@media screen and (max-width:480px) {
  .description{
    &__title{
      line-height: 150%;
      font-size: 13px;
      margin-bottom: 15px;
    }
  }
}
</style>
