<script>
  import AngularCards from "../components/AngularCards.svelte";
  import EmberCards from "../components/EmberCards.svelte";
  import CssGridCards from "../components/CssGridCards.svelte";
</script>

<style>
  @import url("https://fonts.googleapis.com/css?family=Open+Sans:400,600,700");
  @import url("https://use.fontawesome.com/releases/v5.1.0/css/all.css");

  *,
  *::before,
  *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .grid {
    height: auto; /*or 100vh if you want full screen */
    max-width: 800px;
    display: grid;
    grid-template-columns: 65px auto;
    align-items: top;
    justify-content: top;
    padding: 5px;
    font: 14px/1.5 "Open Sans", sans-serif;
  }

  p:not(:last-child) {
    margin: 0 0 20px;
  }

  .box-a,
  .box-b {
    padding: 10px;
    border: 1px solid rgba(0, 0, 0, 0.2);
    color: #fff;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.15);
  }

  .box-a {
    max-width: 60px;
  }

  .box-a-rotate {
    -webkit-transform: rotate(90deg);
    -moz-transform: rotate(90deg);
    -o-transform: rotate(90deg);
    -ms-transform: rotate(90deg);
    transform: rotate(90deg);
  }

  section {
    display: none;
    padding: 20px 0 0;
    border-top: 1px solid #18222e;
  }

  input {
    display: none;
  }

  label {
    display: inline-block;
    margin: 0 0 -1px;
    padding: 15px 25px;
    font-weight: 600;
    text-align: center;
    color: #abc;
    border: 1px solid transparent;
  }

  label:before {
    font-family: fontawesome;
    font-weight: normal;
    margin-right: 10px;
  }

  label[for*="0"]:before {
    font-family: "Font Awesome 5 Brands";
    content: "\f3b9";
    font-size: 40px;
    color: #f0db4f;
  }

  label[for*="1"]:before {
    font-family: "Font Awesome 5 Brands";
    content: "\f41b";
  }
  label[for*="2"]:before {
    font-family: "Font Awesome 5 Brands";
    content: "\f41f";
  }

  label[for*="3"]:before {
    font-family: "Font Awesome 5 Brands";
    content: "\f420";
  }

  label[for*="4"]:before {
    font-family: "Font Awesome 5 Brands";
    content: "\f423";
  }

  label:hover {
    color: #789;
    cursor: pointer;
  }

  input:checked + label[for*="1"] {
    color: #0af;
    border: 1px solid #18222e;
    border-top: 2px solid #0af;
    border-bottom: 1px solid #10161e;
  }

  input:checked + label[for*="2"] {
    color: #42b883;
    border: 1px solid #18222e;
    border-top: 2px solid #42b883;
    border-bottom: 1px solid #10161e;
  }

  input:checked + label[for*="3"] {
    color: #b52e31;
    border: 1px solid #18222e;
    border-top: 2px solid #b52e31;
    border-bottom: 1px solid #10161e;
  }

  input:checked + label[for*="4"] {
    color: #f23819;
    border: 1px solid #18222e;
    border-top: 2px solid #f23819;
    border-bottom: 1px solid #10161e;
  }

  #tab1:checked ~ #content1,
  #tab2:checked ~ #content2,
  #tab3:checked ~ #content3,
  #tab4:checked ~ #content4 {
    display: block;
  }

  @media screen and (max-width: 800px) {
    label {
      font-size: 0;
    }

    label[for*="0"] {
      color: red;
      font-size: 20px;
    }
    label[for*="0"]:before {
      font-family: "Font Awesome 5 Brands";
      content: "\f3b9";
      font-size: 30px;
      color: #f0db4f;
      padding: 5px;
    }

    .box-a {
      padding: 0;
    }

    label:before {
      margin: 0;
      font-size: 18px;
    }
  }

  @media screen and (max-width: 500px) {
    label {
      padding: 18px;
      padding-top: 10px;
      padding-bottom: 10px;
    }
  }

  /* VUE */
  .container {
    height: 300px;
    max-width: 600px;
    top: 60px;
    left: calc(50% - 300px);
    display: flex;
    flex-wrap: wrap;
    margin: 0 auto;
    padding-top: 20px;
  }

  .card-2 {
    height: 20em;
    width: 15em;
    background-color: #17141d;
    border-radius: 10px;
    box-shadow: -1rem 0 3rem #000;
    /*   margin-left: -50px; */
    transition: 0.4s ease-out;
    position: relative;
    left: 0px;
    display: flex;
    max-width: 100%;
    flex-direction: column;
    overflow: hidden;
  }

  .card-2:not(:first-child) {
    margin-left: -50px;
  }

  .card-2:hover {
    transform: translateY(-20px);
    transition: 0.4s ease-out;
  }

  .card-2:hover ~ .card {
    position: relative;
    left: 50px;
    transition: 0.4s ease-out;
  }

  .title {
    color: white;
    font-weight: 300;
    position: absolute;
    left: 20px;
    top: 15px;
  }

  .bar {
    position: absolute;
    top: 100px;
    left: 20px;
    height: 5px;
    width: 150px;
  }

  .emptybar {
    background-color: #2e3033;
    width: 100%;
    height: 100%;
  }

  .filledbar {
    position: absolute;
    top: 0px;
    z-index: 3;
    width: 0px;
    height: 100%;
    background: rgb(0, 154, 217);
    background: linear-gradient(
      90deg,
      rgba(0, 154, 217, 1) 0%,
      rgba(217, 147, 0, 1) 65%,
      rgba(255, 186, 0, 1) 100%
    );
    transition: 0.6s ease-out;
  }

  .card-2:hover .filledbar {
    width: 120px;
    transition: 0.4s ease-out;
  }

  .circle {
    position: absolute;
    top: 150px;
    left: calc(50% - 60px);
  }

  .stroke {
    stroke: white;
    stroke-dasharray: 360;
    stroke-dashoffset: 360;
    transition: 0.6s ease-out;
  }

  svg {
    fill: #17141d;
    stroke-width: 2px;
  }

  .card-2:hover .stroke {
    stroke-dashoffset: 100;
    transition: 0.6s ease-out;
  }

  @media (max-width: 768px) {
    .card-2:not(:first-child) {
      margin-left: 0;
    }
    .card-2:hover:not(:first-child) {
      transform: translateY(-80px);
      transition: 0.4s ease-out;
    }
  }
</style>

<svelte:head>
  <title>Portfolio</title>
</svelte:head>

<main class="grid">
  <div class="box-a" style="font-size: 30px;">
    <div class="box-a-rotate">
      <input id="tab0" type="radio" name="main-tabs" checked />
      <label for="tab0">
        <span style="color: #F0DB4F">JavaScript</span>
      </label>
    </div>
  </div>

  <div class="box-b">
    <input id="tab1" type="radio" name="tabs" checked />
    <label for="tab1">React.JS</label>

    <input id="tab2" type="radio" name="tabs" />
    <label for="tab2">Vue.JS</label>

    <input id="tab3" type="radio" name="tabs" />
    <label for="tab3">Angular.JS</label>

    <input id="tab4" type="radio" name="tabs" />
    <label for="tab4">Ember.JS</label>

    <section id="content1">
      <CssGridCards/>
    </section>

    <section id="content2">

      <div class="container">

        <div class="card-2">
          <h3 class="title">Card 1</h3>
          <div class="bar">
            <div class="emptybar" />
            <div class="filledbar" />
          </div>
          <div class="circle">
            <svg version="1.1" xmlns="http://www.w3.org/2000/svg">
              <circle class="stroke" cx="60" cy="60" r="50" />
            </svg>
          </div>
        </div>

        <div class="card-2">
          <h3 class="title">Card 2</h3>
          <div class="bar">
            <div class="emptybar" />
            <div class="filledbar" />
          </div>
          <div class="circle">
            <svg version="1.1" xmlns="http://www.w3.org/2000/svg">
              <circle class="stroke" cx="60" cy="60" r="50" />
            </svg>
          </div>
        </div>

        <div class="card-2">
          <h3 class="title">Card 3</h3>
          <div class="bar">
            <div class="emptybar" />
            <div class="filledbar" />
          </div>
          <div class="circle">
            <svg version="1.1" xmlns="http://www.w3.org/2000/svg">
              <circle class="stroke" cx="60" cy="60" r="50" />
            </svg>
          </div>
        </div>

      </div>
    </section>

    <section id="content3">
      <AngularCards />
    </section>

    <section id="content4">
      <EmberCards />
    </section>

  </div>
</main>
