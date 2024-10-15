<template>




  <div>


    <div class="hero">
      <div>
        <div class="top">
          <div>
            <div id="output" dir="rtl">
              {{ result }}
            </div>
            <div id="output2" dir="rtl">

            </div>
          </div>
        </div>



        <div class="center bg-dark" id="action">

          <div class="num">
            <button class="btn btn1" id="seven" @click="nam(7)">7</button>
            <button class="btn btn1" id="eight" @click="nam(8)">8</button>
            <button class="btn btn1" id="nine" @click="nam(9)">9</button>
            <button class="btn btn2" id="del">DEL</button>
          </div>

          <div class="num">
            <button class="btn btn1" id="four" @click="nam(4)">4</button>
            <button class="btn btn1" id="five" @click="nam(5)">5</button>
            <button class="btn btn1" id="six" @click="nam(6)">6</button>
            <button class="btn btn1" id="plus" @click="pluss()" value="jam">+</button>
          </div>

          <div class="num">
            <button class="btn btn1" id="one" @click="nam(1)">1</button>
            <button class="btn btn1" id="two" @click="nam(2)">2</button>
            <button class="btn btn1" id="three" @click="nam(3)">3</button>
            <button class="btn btn1" id="menha" @click="menhaa()" value="menha">-</button>
          </div>

          <div class="num">
            <button class="btn btn1" id="dot" @click="nam('.')">.</button>
            <button class="btn btn1" id="zero" @click="nam(0)">0</button>
            <button class="btn btn1" id="slash" @click="taghsim()" value="taghsim">/</button>
            <button class="btn btn1" id="zarb" @click="zarbb()" value="zarb">x</button>
          </div>

          <div class="num">

            <button class="btn btnr" id="reset" @click="res()">reset</button>
            <button class="btn btnmo" id="mosavi" @click="calculate">=</button>




          </div>

        </div>
      </div>
    </div>
















    

  </div>






















</template>

<script>
// let output = document.getElementById('output')



export default {
  data() {
    return {
      expression: '',
      result: '',
      action: '',
      k: '',
      output : ''
    };
  },
  mounted(){
this.output = document.getElementById('output').innerHTML



  },
  methods: {
    calculate() {
      
      
      
      try {
        this.result = eval(output.innerHTML);
      } catch (error) {
        this.result = 'Error';
      }
    },
    nam(number) {


      // document.getElementById("output").innerHTML = ""
      document.getElementById("output").innerHTML += number;
      
console.log(output.innerHTML);


    },
    pluss() {
      this.k = document.getElementById("output").innerHTML
      document.getElementById("output").innerHTML += "+"

    },


    menhaa() {
      this.k = document.getElementById("output").innerHTML
      document.getElementById("output").innerHTML += "-"

    },
    zarbb() {
      this.k = document.getElementById("output").innerHTML
      document.getElementById("output").innerHTML += "*"

    },
    taghsim() {
      this.k = document.getElementById("output").innerHTML
      document.getElementById("output").innerHTML += "/"

    },
    res(){
      document.getElementById("output").innerHTML = '  '
    }

  }
};
</script>


<style>
html,
body {
  height: 100%;
  margin: 0px;
}

body {
  background-color: rgb(57, 45, 92);
}

.hero {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;


}

.hero>div {
  width: 30%;
  /* height: 100%; */


}

.top {
  direction: rtl;
  border-radius: .5rem;
  background-color: rgb(26, 24, 24);
  margin-top: 2rem;
  height: 120px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.top>div {
  width: 90%;
  font-size: 3rem;
  color: white;
}

.center {
  padding-top: .4rem;
  padding-bottom: .4rem;
  margin-top: 2rem;
  /* height: 400px; */
  width: 100%;
  border-radius: .5rem;

}

.num {
  z-index: 2;
  width: 100%;
  height: 68px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.btn1 {
  font-size: 1.3rem;
  font-weight: bold;
  width: 17%;
  background-color: white !important;
  transition: all .3s ease-in-out;
}

.btn1:hover {
  background-color: rgba(255, 255, 255, 0.589) !important;
}

.btn2 {
  font-size: 1rem;
  padding-top: 12px;
  font-weight: bold;
  padding-bottom: 12px;
  width: 17%;
  background-color: darkslategray;
  color: white !important;
}

.btnr {
  font-size: 1.3rem;
  font-weight: bold;
  width: 43%;
  background-color: darkslategray;
  color: white !important;
}

.btnmo {
  font-size: 1.3rem;
  font-weight: bold;
  width: 43%;
  background-color: red;
  color: white !important;

}
</style>