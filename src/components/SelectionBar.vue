<template>
  <div>
    <div class="slidecontainer">
      <input v-model="position" type="range" min="1" max="10" value="5" class="slider" id="myRange">
    </div>
    <div>
      <p v-if="position == 1">{{ position }} Digit Long</p>
      <p v-else>{{ position }} Digits Long</p>
      <p>Your Random Number: </p><p class="my-random">{{ result }}</p>
      <button @click="refreshCurrent" class="btn new-random"><i class="fa fa-retweet fa-2x"></i></button>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      position: 5,
      result: null
    }
  },
  watch: {
    position: function (value) {
      var myNum = Number(value)

      if (myNum === 1) {
        this.returnOneDigit()
      } else if (myNum === 2) {
        this.returnTwoDigit()
      } else if (myNum === 3) {
        this.returnThreeDigit()
      } else if (myNum === 4) {
        this.returnFourDigit()
      } else if (myNum === 5) {
        this.returnFiveDigit()
      } else if (myNum === 6) {
        this.returnSixDigit()
      } else if (myNum === 7) {
        this.returnSevenDigit()
      } else if (myNum === 8) {
        this.returnEightDigit()
      } else if (myNum === 9) {
        this.returnNineDigit()
      } else if (myNum === 10) {
        this.returnTenDigit()
      }
    }
  },
  methods: {
    refreshCurrent () {
      var myNum = Number(this.position)

      if (myNum === 1) {
        this.returnOneDigit()
      } else if (myNum === 2) {
        this.returnTwoDigit()
      } else if (myNum === 3) {
        this.returnThreeDigit()
      } else if (myNum === 4) {
        this.returnFourDigit()
      } else if (myNum === 5) {
        this.returnFiveDigit()
      } else if (myNum === 6) {
        this.returnSixDigit()
      } else if (myNum === 7) {
        this.returnSevenDigit()
      } else if (myNum === 8) {
        this.returnEightDigit()
      } else if (myNum === 9) {
        this.returnNineDigit()
      } else if (myNum === 10) {
        this.returnTenDigit()
      }
    },
    returnOneDigit () {
      this.result = Math.floor(1 + Math.random() * 9)
    },
    returnTwoDigit () {
      this.result = Math.floor(10 + Math.random() * 90)
    },
    returnThreeDigit () {
      this.result = Math.floor(100 + Math.random() * 900)
    },
    returnFourDigit () {
      this.result = Math.floor(1000 + Math.random() * 9000)
    },
    returnFiveDigit () {
      this.result = Math.floor(10000 + Math.random() * 90000)
    },
    returnSixDigit () {
      this.result = Math.floor(100000 + Math.random() * 900000)
    },
    returnSevenDigit () {
      this.result = Math.floor(1000000 + Math.random() * 9000000)
    },
    returnEightDigit () {
      this.result = Math.floor(10000000 + Math.random() * 90000000)
    },
    returnNineDigit () {
      this.result = Math.floor(100000000 + Math.random() * 900000000)
    },
    returnTenDigit () {
      this.result = Math.floor(1000000000 + Math.random() * 9000000000)
    }
  }
}
</script>

<style>
.slidecontainer {
    width: 100%;
}

.slider {
    -webkit-appearance: none;
    width: 33em;
    height: 2.3em;
    background: #feee7d;
    border: 0.3em solid #ef5285;
    opacity: 0.7;
    -webkit-transition: .2s;
    transition: opacity .2s;
}
.slider:hover {
    opacity: 1;
}

.slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 2.3em;
    height: 2.3em;
    background: #ef5285;
    cursor: pointer;
}

.slider::-moz-range-thumb {
    width: 2.3em;
    height: 2.3em;
    background: #ef5285;
    cursor: pointer;
}
.my-random {
  font-weight: bold;
  font-size: 3em;
  margin: 0;
}
.new-random {
  width: 6em;
  height: 3em;
  border-radius: 4em;
  color: #ef5285;
  background-color: #feee7d;
}
</style>
