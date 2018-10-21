<template>
  <div class="tabs__wrapper">
    <input name="tabs" type="radio" id="tabLeft" checked>
		<input name="tabs" type="radio" id="tabRight">
    <div class="tabs">
			<label class="tabs__label" for="tabLeft">One</label>
			<label class="tabs__label" for="tabRight">Two</label>
		</div>
    <div class="tabs__block tabs__block--one">
      Первый блок
    </div>
    <div class="tabs__block tabs__block--two">
      Второй блок
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tabs',
};
</script>

<style lang="scss" scoped>
input[name="tabs"] {
  display: none;
}

.tabs {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  border-radius: 20px;
  margin: 5px auto 20px;
}

.tabs__label {
  color: #000;
  font-weight: normal;
  font-size: 14px;
  text-align: center;

  width: 50%;
  padding: 10px 2px;
  background-color: #cecece;
  transition: background-color 0.1s ease;
  cursor: pointer;
}

#tabLeft:checked ~ .tabs .tabs__label[for="tabLeft"] {
  color: #fff;
  font-weight: 900;
  background-color: lightpink;
  box-shadow: lightgreen;
}

#tabMiddle:checked ~ .tabs .tabs__label[for="tabMiddle"] {
  color: #fff;
  font-weight: 900;
  background-color: lightpink;
  box-shadow: lightgreen;
}

#tabRight:checked ~ .tabs .tabs__label[for="tabRight"] {
  color: #fff;
  font-weight: 900;
  background-color: lightgreen;
}

#tabLeft:checked ~ {
  .tabs__block--one {
    display: block;
  }
  .tabs__block--two {
    display: none;
  }
}

#tabRight:checked ~ {
  .tabs__block--one {
    display: none;
  }
  .tabs__block--two {
    display: block;
  }
}
</style>
