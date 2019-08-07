<svelte:head>
	<title>About</title>
</svelte:head>


<style>
		@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,600,700');
		@import url('https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css');

		*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
		html,body{height:100vh;}
		body{
		display:flex;
		align-items:center;
		justify-content:center;
		padding:40px;
		font:14px/1.5 'Open Sans', sans-serif;
		}

		p:not(:last-child) {
			margin: 0 0 20px;
		}

		main {
			max-width: 800px;
			padding: 40px;
			border: 1px solid rgba(0,0,0,.2);
			color: #fff;
			box-shadow: 0 1px 3px rgba(0,0,0,.15);
		}

		section {
			display: none;
			padding: 20px 0 0;
			 border-top: 1px solid #18222E;
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

		label[for*='1']:before { content: '\f41b'; }
		label[for*='2']:before { content: '\f17d'; }
		label[for*='3']:before { content: '\f16c'; }
		label[for*='4']:before { content: '\f171'; }

		label:hover {
			color: #789;
			cursor: pointer;
		}

		input:checked + label {
			color: #0af;
			border: 1px solid #18222E;
			border-top: 2px solid #0af;
			border-bottom: 1px solid #10161E;
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




<main>

  <input id="tab1" type="radio" name="tabs" checked>
  <label for="tab1">Codepen</label>

  <input id="tab2" type="radio" name="tabs">
  <label for="tab2">Dribbble</label>

  <input id="tab3" type="radio" name="tabs">
  <label for="tab3">Stack Overflow</label>

  <input id="tab4" type="radio" name="tabs">
  <label for="tab4">Bitbucket</label>

  <section id="content1">
    <p>
      Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
    </p>
    <p>
      Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
    </p>
  </section>

  <section id="content2">
    <p>
      Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
    </p>
    <p>
      Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
    </p>
  </section>

  <section id="content3">
    <p>
      Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
    </p>
    <p>
      Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
    </p>
  </section>

  <section id="content4">
    <p>
      Bacon ipsum dolor sit amet landjaeger sausage brisket, jerky drumstick fatback boudin.
    </p>
    <p>
      Jerky jowl pork chop tongue, kielbasa shank venison. Capicola shank pig ribeye leberkas filet mignon brisket beef kevin tenderloin porchetta. Capicola fatback venison shank kielbasa, drumstick ribeye landjaeger beef kevin tail meatball pastrami prosciutto pancetta. Tail kevin spare ribs ground round ham ham hock brisket shoulder. Corned beef tri-tip leberkas flank sausage ham hock filet mignon beef ribs pancetta turkey.
    </p>
  </section>

</main>