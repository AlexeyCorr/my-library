<template>
  <div class="rating">
    <svg xmlns="http://www.w3.org/2000/svg" style="display: none"><symbol id="star" viewbox="0 0 19.481 19.481"><path d="M10.201.758l2.478 5.865 6.344.545a.5.5 0 0 1 .285.876l-4.812 4.169 1.442 6.202a.5.5 0 0 1-.745.541l-5.452-3.288-5.452 3.288a.5.5 0 0 1-.745-.541l1.442-6.202-4.813-4.17a.5.5 0 0 1 .285-.876l6.344-.545L9.28.758a.5.5 0 0 1 .921 0z"/></symbol></svg>

    <input class="rating__input" type="radio" name="rating" id="ratingStar5">
    <label class="rating__label" for="ratingStar5">
      <svg width="33" height="33">
        <use xlink:href="#star"></use>
      </svg>
    </label>
     <input class="rating__input" type="radio" name="rating" id="ratingStar4">
    <label class="rating__label" for="ratingStar4">
      <svg width="33" height="33">
        <use xlink:href="#star"></use>
      </svg>
    </label>
    <input class="rating__input" type="radio" name="rating" id="ratingStar3">
    <label class="rating__label" for="ratingStar3">
      <svg width="33" height="33">
        <use xlink:href="#star"></use>
      </svg>
    </label>
    <input class="rating__input" type="radio" name="rating" id="ratingStar2">
    <label class="rating__label" for="ratingStar2">
      <svg width="33" height="33">
        <use xlink:href="#star"></use>
      </svg>
    </label>
    <input class="rating__input" type="radio" name="rating" id="ratingStar1">
    <label class="rating__label" for="ratingStar1">
      <svg width="33" height="33">
        <use xlink:href="#star"></use>
      </svg>
    </label>
  </div>
</template>

<script>
export default {
  name: 'Rating',
};
</script>

<style lang="scss" scoped>
.rating {
  width: 165px;
  margin: 50px auto;
  display: flex;
  justify-content: space-between;
  flex-direction: row-reverse;

  .rating__label svg {
    fill: transparent;
    stroke: grey;
  }
}

.rating__input {
  display: none;

  &:checked + .rating__label svg,
  &:checked ~ .rating__label svg {
    fill: lightgreen;
    stroke: lightgreen;
  }
}

.rating {
  .rating__label {
  cursor: pointer;
    svg {
      transition: all 0.2s ease;
    }

    &:hover ~ .rating__label svg {
      fill: lightgreen;
      stroke: lightgreen;
    }

    svg:hover {
      fill: lightgreen;
      stroke: lightgreen;
    }
  }
}
</style>
