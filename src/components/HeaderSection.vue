<template>
  <div class="section">
    <h1 class="section__heading">{{ title }}</h1>
    <p class="section__paragraph">{{ desc }}</p>
  </div>
</template>
<script>
export default {
  props:['title', 'desc']
};
</script>
<style lang="scss" scoped>
.section {
  background: #151b3d;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;

  &__heading {
    font-weight: 700;
    font-size: 40px;
    line-height: 47px;
    color: #ffffff;
    padding: 98px 0 27px 0;
  }

  &__paragraph {
    font-weight: 300;
    max-width: 55%;
    font-size: 15px;
    line-height: 22px;
    color: #ffffff;
  }
}
</style>
