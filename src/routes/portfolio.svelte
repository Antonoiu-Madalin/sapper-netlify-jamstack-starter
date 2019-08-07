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
    max-width: 900px;
    display: grid;
    grid-template-columns: 100px auto;
    grid-gap: 10px;
    align-items: top;
    justify-content: top;
    padding: 20px;
    font: 14px/1.5 "Open Sans", sans-serif;
  }

  p:not(:last-child) {
    margin: 0 0 20px;
  }

  .box-a,
  .box-b {
    padding: 40px;
    border: 1px solid rgba(0, 0, 0, 0.2);
    color: #fff;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.15);
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
    label:before {
      margin: 0;
      font-size: 18px;
    }
  }

  @media screen and (max-width: 500px) {
    label {
      padding: 15px;
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

      <ul style="padding-left: 17px">
        <li>Gatsby.js</li>
        <li>Next.js</li>
      </ul>
      <br />
      <p>
        Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig
        ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta.
        Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger
        beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare
        ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip
        leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
      </p>
      <p>
        Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick
        fatback boudin.
      </p>
    </section>

    <section id="content2">
      <p>
        Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick
        fatback boudin.
      </p>
      <p>
        Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig
        ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta.
        Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger
        beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare
        ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip
        leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
      </p>
    </section>

    <section id="content3">
      <p>
        Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig
        ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta.
        Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger
        beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare
        ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip
        leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
      </p>
      <p>
        Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick
        fatback boudin.
      </p>
    </section>

    <section id="content4">
      <p>
        Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick
        fatback boudin.
      </p>
      <p>
        Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig
        ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta.
        Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger
        beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare
        ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip
        leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
      </p>
    </section>
  </div>
</main>

<!-- Make radio and chose based on JavaScript, Php etc to show, with {#if}-->
<!--<main class="grid">
		<div class="box-a" style="font-size: 30px;">
			<div class="box-a-rotate">
				<input id="tab10" type="radio" name="main-tabs-secondary">
				<label for="tab10"><span style="color: #4f5b93;">PHP</span></label>
			</div>
		</div>

		<div class="box-b">
			<input id="tab11" type="radio" name="tabs-secondary">
			<label for="tab11">Laravel</label>

			<input id="tab12" type="radio" name="tabs-secondary">
			<label for="tab12">Vue</label>

			<input id="tab13" type="radio" name="tabs-secondary">
			<label for="tab13" >Angular</label>

			<input id="tab14" type="radio" name="tabs-secondary">
			<label for="tab14">PHP</label>

			<section id="content11">

					<ul style="padding-left: 17px">
						<li>Gatsby.js</li>
						<li>Next.js</li>
					</ul>
					<br>
					<p>
						Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
					</p>
					<p>
						Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
					</p>
			</section>

			<section id="content12">
				<p>
					Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
				</p>
				<p>
					Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
				</p>
			</section>

			<section id="content13">
				<p>
					Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
				</p>
				<p>
					Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
				</p>
			</section>

			<section id="content14">
				<p>
					Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
				</p>
				<p>
					Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
				</p>
			</section>
	</div>
</main>-->
