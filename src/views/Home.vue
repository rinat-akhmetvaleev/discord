<template>
  <div class="home">
    <div>
      <div class="f">
        <div class="burger">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <full-page ref="fullpage" :options="options" id="fullpage">
        <div class="section">
            <div class="wrap">
                <div class="container">
                    <img src="../assets/icon/logo 1.png" alt="logo">
                </div>
            </div>
        </div>
        <div class="section">
            <div class="content">
                <div class="left">
                  <div class="left_wrap">
                    <div class="img_wrap">
                      <img src="../assets/icon/voice.svg" alt="voice logo">
                    </div>
                  </div>
                </div>
                <div class="right">
                    <h1>Voice</h1>
                    <p>Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</p>
                </div>
            </div>
        </div>
        <div class="section">
            <div class="content">
                <div class="left">
                  <div class="left_wrap">
                    <div class="img_wrap">
                      <img src="../assets/icon/text.svg" alt="Text logo">
                    </div>
                  </div>
                </div>
                <div class="right">
                    <h1>Text</h1>
                    <p>Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</p>
                </div>
            </div></div>
        <div class="section">
            <div class="content">
                <div class="left">
                  <div class="left_wrap">
                    <div class="img_wrap">
                      <img src="../assets/icon/connect.svg" alt="Connect logo">
                    </div>
                  </div>
                </div>
                <div class="right">
                    <h1>Connect</h1>
                    <p>Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</p>
                </div>
            </div>
        </div>
      </full-page>
    </div>
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  data() {
    return {
      options: {
        licenseKey: "YOUR_KEY_HERE",
        menu: "#myMenu",
        anchors: ["page1", "page2", "page3", "page4"],
        sectionsColor: ["#181818", "#181818", "#181818", "#181818"],
        afterLoad: this.afterLoad,
      },
    };
  },
  methods: {
    afterLoad(destination, origin) {
      console.log(destination, origin);
      console.log("Emitted 'after load' event.");
      // if (origin.anchor == "page1") {
      //   alert("Section 1 ended loading");
      // }
      //  if (origin.anchor == "page2") {
      //   alert("Section 2 ended loading");
      // }
      //  if (origin.anchor == "page3") {
      //   alert("Section 3 ended loading");
      // }
      //  if (origin.anchor == "page4") {
      //   alert("Section 4 ended loading");
      // }
    },
  },
};
</script>

<style>
.f {
  position: absolute;
  left: 25px;
  top: 50px;
  z-index: 5;
  color: white;
}

.burger span {
  width: 55px;
  height: 1px;
  background: white;
  position: absolute;
}
/* burger close menu */
span:nth-child(1) {
  top: -15px;
}
span:nth-child(3) {
  top: 15px;
}

/* burger open menu 
span:nth-child(2){
  display: none;
}
*/
.wrap {
  display: flex;
}

.container {
  width: 40%;
  height: 350px;
  border: 50px solid #828282;
  box-shadow: inset 4px 4px 30px #ccc;
  margin: 250px auto;
  display: flex;
  align-content: center;
  justify-content: center;
  align-items: center;
}

.right,
.left{
  margin: 250px auto;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}

.right{
  position: relative;
  z-index: 2;
}

.right::before{
  content: '';
  width: 150px;
  height: 100px;
  border: 5px solid rgba(255, 230, 0, 0.24);
  position: absolute;
  z-index: 1;
  top: -50px;
  right: 200px;
}

h1{
  font-weight: 600;
  font-size: 64px;
  line-height: 78px;
  color: #EBEBEB;
}

p{
  width: 700px;
  color: #A1A1A1;
  font-weight: 600;
  font-size: 24px;
  line-height: 29px;
  text-align: left;
}

.content{
  display: flex;
  justify-content: space-evenly;
}

.left_wrap img{
  width: 115px;
  height: 115px;
  padding: 1em 1em;
}

.left_wrap{
  border-radius: 50%;
  background: linear-gradient(to top, #ECD820, #fff);
  width: 285px;
  height: 285px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.img_wrap {
  border-radius: 50%;
  padding: 4em 4em;
  background-color: rgb(24, 24, 24);
}
</style>
