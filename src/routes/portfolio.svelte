<script>
  import ReactCards from "../components/ReactCards.svelte";
  import VueCards from "../components/VueCards.svelte";
  import AngularCards from "../components/AngularCards.svelte";
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
    position: -webkit-sticky;
    position: sticky;
    top: 0;
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

    <section id="content1" class="ReactCards">
      <ReactCards />
    </section>

    <section id="content2" class="VueCards">
      <VueCards />
    </section>

    <section id="content3" class="AngularCards">
      <AngularCards />
    </section>

    <section id="content4">
      <ReactCards />
    </section>

  </div>
</main>
