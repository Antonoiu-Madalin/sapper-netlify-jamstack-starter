<style>
  /* To give card different colour filling, change .card background and card_svg path first option*/
  * {
    box-sizing: border-box;
    line-height: 1.5;
    font-family: "Open Sans", sans-serif;
  }
  a {
    text-decoration: inherit; /* no underline */
    color: inherit;
  }

  img {
    height: auto;
    max-width: 100%;
  
    background-size: cover;
    background-repeat: no-repeat;
    
  }
  .container {
    display: flex;
    flex-wrap: wrap;
    margin: 0 auto;
    max-width: 1200px;
  }
  .cards_item {
    display: flex;
    padding: 1rem;
    list-style: none;
  }

  .card {
    position: relative;
    background: #fc6621; /*Specific to React content part, not svg #42b883 , #fc6621; svelte , #42b883 vue*/
    display: flex;
    border-radius: 6px;
    color: #151d28;
    overflow: hidden;
    flex-direction: column;
    opacity: 1; max-height:40rem;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  }
  .card:hover{
     box-shadow: 0 7px 14px#fc6621, 0 10px 10px rgba(0, 0, 0, 0.22);
  }


  .card__line {
    opacity: 1;
   
  }

  .card__content{
    padding: 0 10px;
 
  }

  .card__svg {
  position: absolute; 
  top:11.5%;
  }
  .card__title {
    color: #151d28;
    font-weight: 800;
    letter-spacing: 0.01em;
    z-index: 9999999;
  }


  @media (max-width: 370px) {
    .card__title { font-size: 125%; margin-top: 8px;}
   
  }
   @media (max-width: 30rem) {
    .card__svg{top:14.5%;}
    .container {margin: 0;}
   }
   @media (min-width: 30rem) {
    .card__svg{top:16.1%;}
    .container {margin: 0 40px;}
    .card__title { margin-top: 12px;}
  }
  @media (min-width: 40rem) {
    .card__svg{top:14.3%}
    .cards_item {width: 50%}
    .container {margin: 0}
  }
  @media (min-width: 56rem) {
    .card__svg{top:11.6%;}
    .cards_item {width: 33.3333%;}
    .container {margin: 0;}
    img {
      min-height:161px;
    }
  }

  /*Blur */

  .blur_grayscale {
    -webkit-filter: blur(5px) grayscale(1);
    -moz-filter: blur(5px) grayscale(1);
    -o-filter: blur(5px) grayscale(1);
    -ms-filter: blur(5px) grayscale(1);
    filter: blur(5px) grayscale(1);
    max-width: 100%;
    height: auto;
    background-color: #090a0f;
    z-index: 9999;
    /*noselect*/
    -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
    -khtml-user-select: none; /* Konqueror HTML */
    -moz-user-select: none; /* Firefox */
    -ms-user-select: none; /* Internet Explorer/Edge */
    user-select: none; /* Non-prefixed version, currently
                                                                      supported by Chrome and Opera */
    /*cursor: not-allowed;*/
  }
  .mouseover_pointer {
    cursor: pointer;
  }
</style>

<div class="container">

  <li class="cards_item mouseover_pointer">
 
    <div class="card">
     <a href="/portfolio">
      <div class="card__image-container">
        <img
          class="card__image"
          src="https://images.unsplash.com/photo-1526948128573-703ee1aeb6fa?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=351&ixid=eyJhcHBfaWQiOjF9&ixlib=rb-1.2.1&q=80&w=439"
          alt="" />
      </div>

      <svg class="card__svg" viewBox="0 0 800 500">

        <path
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400 L 800 500 L 0 500"
          stroke="transparent"
          fill="#fc6621" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="black"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">Portfolio</h1>
         
        <hr>
          <p>
          This portfolio website has been built with <strong>Svelte.js</strong> and <strong>Sapper</strong>.
          </p>
       
      </div>
      </a>
    </div>
  
  </li>

  <li class="cards_item blur_grayscale">
    <div class="card">
      <div class="card__image-container">
        <img
          class="card__image"
          src="https://images.unsplash.com/photo-1560202212-441ad59100fd?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=351&ixid=eyJhcHBfaWQiOjF9&ixlib=rb-1.2.1&q=80&w=439"
          alt="" />
      </div>

      <svg class="card__svg" viewBox="0 0 800 500">

        <path
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400 L 800 500 L 0 500"
          stroke="transparent"
          fill="#fc6621" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="pink"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">Pizzeria</h1>
        
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor
          praesentium at quod autem omnis.
        </p>
      </div>
      </div>
  
  </li>

  <li class="cards_item blur_grayscale">
    <div class="card">
      <div class="card__image-container">
        <img
          class="card__image"
          src="https://images.unsplash.com/photo-1542426144-3e6c375380e9?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=351&ixid=eyJhcHBfaWQiOjF9&ixlib=rb-1.2.1&q=80&w=439"
          alt="" />
      </div>

      <svg class="card__svg" viewBox="0 0 800 500">

        <path
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400 L 800 500 L 0 500"
          stroke="transparent"
          fill="#fc6621" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="pink"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">Blogging</h1>
        
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor
          praesentium at quod autem omnis.
        </p>
        </div>
     
    </div>
  </li>

  <li class="cards_item blur_grayscale">
    <div class="card">
      <div class="card__image-container">
        <img
          class="card__image"
          src="https://picsum.photos/id/435/439/351"
          alt="" />
      </div>

      <svg class="card__svg" viewBox="0 0 800 500">

        <path
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400 L 800 500 L 0 500"
          stroke="transparent"
          fill="#fc6621" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="pink"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">Personal</h1>
     
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor
          praesentium at quod autem omnis.
        </p>
      </div>
      
    </div>
  </li>

  <li class="cards_item blur_grayscale">
    <div class="card">
      <div class="card__image-container">
        <img
          class="card__image"
          src="https://images.unsplash.com/photo-1532347921492-89bea98a0c6d?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=351&ixid=eyJhcHBfaWQiOjF9&ixlib=rb-1.2.1&q=80&w=439"
          alt="" />
      </div>

      <svg class="card__svg" viewBox="0 0 800 500">

        <path
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400 L 800 500 L 0 500"
          stroke="transparent"
          fill="#fc6621" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="pink"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">Book-like</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor
          praesentium at quod autem omnis.
        </p>
      </div>
    </div>
  </li>

  <li class="cards_item blur_grayscale">
    <div class="card">
      <div class="card__image-container">
        <img
          class="card__image"
          src="https://picsum.photos/id/79/439/351"
          alt="" />
      </div>

      <svg class="card__svg" viewBox="0 0 800 500">

        <path
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400 L 800 500 L 0 500"
          stroke="transparent"
          fill="#fc6621" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="pink"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">Travelling</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor
          praesentium at quod autem omnis.
        </p>
      </div>
    </div>
  </li>


</div>
