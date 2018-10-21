<template>
  <div class="burger-toggle__wrapper">
    <button class="burger" :class="[isOpen ? 'burger--opened' : '']" type="button" @click="openMenu">
      <span></span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'BurgerToggle',
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    openMenu() {
      if (!this.isOpen) {
        this.isOpen = true;
      } else {
        this.isOpen = false;
      }
    },
  },
}


</script>

<style lang="scss" scoped>
  .burger {
    position: relative;
    width: 30px;
    height: 30px;
    border: none;
    padding: 0;
    background-color: transparent;
    cursor: pointer;

    span {
      position: relative;
      display: block;
      width: 30px;
      height: 3px;
      background-color: #000;

      &::before,
      &::after {
        content: "";
        position: absolute;
        left: 0;
        width: 100%;
        height: 3px;
        background-color: #000;
        transform-origin: 50% 50%;
        transition: top 0.3s 0.3s, transform 0.3s;
      }

      &::after {
        top: -10px;
      }

      &::before {
        top: 10px;
      }
    }
  }

  .burger--opened {
    span {
      background-color: transparent;
      &::after {
        transform: rotate(45deg);
      }

      &::before {
        transform: rotate(-45deg);
      }

      &::before,
      &::after {
        top: 0;
        transition: top 0.3s, transform 0.3s  0.3s;
      }
    }
  }
</style>
