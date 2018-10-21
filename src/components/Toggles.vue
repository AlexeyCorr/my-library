<template>
  <div class="toggles">
    <div class="toggles__row">
      <div class="toggle__wrapper">
        <input class="toggle__check" type="checkbox" id="checkbox-one" name="checkbox-one">
        <div class="toggle">
          <label class="toggle__label" for="checkbox-one"></label>
        </div>
      </div>
    </div>
    <div class="toggles__row">
      <div class="radio-btn">
				<input type="radio" id="regMan" name="regGender" required checked>
				<label for="regMan">М</label>
				<input type="radio" id="regWoman" name="regGender" required>
				<label for="regWoman">Ж</label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Toggles',
};
</script>

<style lang="scss" scoped>
.toggles__row {
  margin: 0 0 15px;
}

.toggle {
  position: relative;
  margin: 0 0 5px 10px;
  width: 50px;
  height: 30px;
  background-color: #fff;
  border-radius: 20px;
  border: 2px solid #eee;
  transition: all 0.2s ease-in-out;
}

.toggle__check {
  display: none;
}

.toggle__label {
  position: absolute;
  left: 0;
  top: 0;

  display: block;
  width: 26px;
  height: 26px;
  border-radius: 50%;
  background-color: lightpink;
  box-shadow: #eee;
  transition: all 0.2s ease-in-out;
  cursor: pointer;
}

.toggle__check:checked + .toggle {
  background-color: lightpink;
  border-color: lightpink;

  .toggle__label {
    left: 20px;
    background-color: #fff;
  }
}

.radio-btn {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 120px;

  input {
    display: none;
  }

  label {
    font-weight: 700;
    line-height: 1;
    color: #000;

    display: block;
    background-color: #fff;
    box-shadow: #eee;
    border-radius: 20px;
    border: 1px solid #eee;
    padding: 10px 15px;
    cursor: pointer;
  }

  input:checked + label {
    color: #009688;
    box-shadow: 0px 2px 10px #009688;
  }
}

</style>
