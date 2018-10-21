<template>
  <div>
    <h1 class="title">Заголовок</h1>
  </div>
</template>

<script>
export default {
  name: 'MainTitle',
};
</script>

<style lang="scss" scoped>
.title {
  color: #9264a1;
  font-size: 22px;
  line-height: 1.3;
  font-weight: 700;
  text-align: center;
  text-transform: uppercase;

  display: flex;
  align-items: center;
  margin: 0 0 15px;

  &::before,
  &::after {
    content: "";
    width: 10px;
    height: 3px;
    flex-grow: 1;
    flex-shrink: 0;
    background-color: #9264a1;
  }

  &::before {
    margin-right: 10px;
  }

  &::after {
    margin-left: 10px;
  }
}
</style>
