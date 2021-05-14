<template>
  <div class="middle">
    <div class="multi-range-slider">
      <input id="input-left" type="range" min="0" max="100" value="0" />
      <input id="input-right" type="range" min="0" max="100" value="100" />

      <div class="slider">
        <div class="track"></div>
        <div class="range"></div>
        <div class="thumb left"></div>
        <div class="thumb right"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const inputLeft = document.getElementById('input-left')
    const inputRight = document.getElementById('input-right')

    const thumbLeft = document.querySelector('.slider > .thumb.left')
    const thumbRight = document.querySelector('.slider > .thumb.right')
    const range = document.querySelector('.slider > .range')

    function setLeftValue() {
      const _this = inputLeft
      const min = parseInt(_this.min)
      const max = parseInt(_this.max)

      _this.value = Math.min(
        parseInt(_this.value),
        parseInt(inputRight.value) - 1
      )

      const percent = ((_this.value - min) / (max - min)) * 100

      thumbLeft.style.left = percent + '%'
      range.style.left = percent + '%'
    }
    setLeftValue()

    function setRightValue() {
      const _this = inputRight
      const min = parseInt(_this.min)
      const max = parseInt(_this.max)

      _this.value = Math.max(
        parseInt(_this.value),
        parseInt(inputLeft.value) + 1
      )

      const percent = ((_this.value - min) / (max - min)) * 100

      thumbRight.style.right = 100 - percent + '%'
      range.style.right = 100 - percent + '%'
    }
    setRightValue()

    inputLeft.addEventListener('input', setLeftValue)
    inputRight.addEventListener('input', setRightValue)

    inputLeft.addEventListener('mouseover', function () {
      thumbLeft.classList.add('hover')
    })
    inputLeft.addEventListener('mouseout', function () {
      thumbLeft.classList.remove('hover')
    })
    inputLeft.addEventListener('mousedown', function () {
      thumbLeft.classList.add('active')
    })
    inputLeft.addEventListener('mouseup', function () {
      thumbLeft.classList.remove('active')
    })

    inputRight.addEventListener('mouseover', function () {
      thumbRight.classList.add('hover')
    })
    inputRight.addEventListener('mouseout', function () {
      thumbRight.classList.remove('hover')
    })
    inputRight.addEventListener('mousedown', function () {
      thumbRight.classList.add('active')
    })
    inputRight.addEventListener('mouseup', function () {
      thumbRight.classList.remove('active')
    })
  },
}
</script>

<style lang="scss" scoped>
.middle {
  position: relative;
  max-width: 400px;
}

.slider {
  position: relative;
  z-index: 1;
  height: 5px;
  margin: 0 15px;
}
.slider > .track {
  position: absolute;
  z-index: 1;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  border-radius: 5px;
  background-color: #c6aee7;
}
.slider > .range {
  position: absolute;
  z-index: 2;
  left: 25%;
  right: 25%;
  top: 0;
  bottom: 0;
  border-radius: 5px;
  background-color: #6200ee;
}
.slider > .thumb {
  position: absolute;
  z-index: 3;
  width: 15px;
  height: 15px;
  background-color: #6200ee;
  border-radius: 50%;
  box-shadow: 0 0 0 0 rgba(98, 0, 238, 0.1);
  transition: box-shadow 0.3s ease-in-out;
}
.slider > .thumb.left {
  left: 25%;
  transform: translate(-10px, -6px);
}
.slider > .thumb.right {
  right: 25%;
  transform: translate(1px, -6px);
}
.slider > .thumb.hover {
  box-shadow: 0 0 0 10px rgba(98, 0, 238, 0.1);
}
.slider > .thumb.active {
  box-shadow: 0 0 0 15px rgba(98, 0, 238, 0.2);
}

input[type='range'] {
  position: absolute;
  pointer-events: none;
  -webkit-appearance: none;
  z-index: 2;
  height: 5px;
  width: 100%;
  opacity: 0;
}
input[type='range']::-webkit-slider-thumb {
  pointer-events: all;
  width: 30px;
  height: 30px;
  border-radius: 0;
  border: 0 none;
  background-color: red;
  -webkit-appearance: none;
}
</style>
