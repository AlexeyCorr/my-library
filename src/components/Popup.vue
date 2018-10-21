<template>
  <div>
    <button class="button" @click="openPopup">
      Показать модальное окно
    </button>

    <div class="popup__wrapper" :class="[popupOpen ? 'popup__wrapper--visibility' : '']">
      <div class="popup">
        <button class="popup__close" title="Закрыть" @click="openPopup"></button>
        <h3>Заголовок</h3>
        <p>Описание</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Popup',
  data() {
    return {
      popupOpen: false,
    }
  },
  methods: {
    openPopup() {
      if (!this.popupOpen) {
        this.popupOpen = true;
      } else {
        this.popupOpen = false;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.popup__wrapper {
  display: none;
  position: fixed;
  justify-content: center;
  align-items: center;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 50;
  background-color: rgba(0,0,0,0.5);

  &--visibility {
    animation: visible 0.2s ease-in-out;
    display: flex;
  }
}

.popup {
  position: relative;
  z-index: 100;
  padding: 15px;
  max-width: 640px;
  min-width: 320px;
  background-color: #fff;
}

.popup__close {
  position: absolute;
  top: 2px;
  right: 2px;
  display: block;
  width: 25px;
  height: 25px;
  min-height: 25px;
  border: none;
  background-color: transparent;
  cursor: pointer;

  &::before,
  &::after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100%;
    height: 2px;
    background-color: #000;
    transition: background-color 0.2s ease-in-out;
  }

  &::before {
    transform: translate(-50%, -50%) rotate(45deg);
  }

  &::after {
    transform: translate(-50%, -50%) rotate(-45deg);
  }

  &:hover,
  &:focus {
    &::before,
    &::after {
      background-color: #9e9e9e;
    }
  }
}

@keyframes visible {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
