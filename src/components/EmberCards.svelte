<style>
  * {
    box-sizing: border-box;
    line-height: 1.5;
    font-family: "Open Sans", sans-serif;
  }
  img {
    height: auto;
    max-width: 100%;
    vertical-align: middle;
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
    background: #333;
    display: flex;
    border-radius: 6px;
    color: #aaa;
    box-shadow: 0 0.25rem 0.25rem rgba(0, 0, 0, 0.2), 0 0 1rem rgba(0, 0, 0, 0.2);
    overflow: hidden;
    flex-direction: column;
  }
  .card__image-container {
    margin: auto;
  }
  .card__line {
    opacity: 0;
    animation: LineFadeIn 0.8s 0.8s forwards ease-in;
  }
  .card__image {
    opacity: 0;
    animation: ImageFadeIn 0.8s 1.4s forwards;
  }
  .card__title {
    color: white;
    font-weight: 800;
    letter-spacing: 0.01em;
  }
  .card__content {
    margin-top: -10rem;
    opacity: 0;
    animation: ContentFadeIn 0.8s 1.6s forwards;
    padding: 0 10px;
  }
  .card__svg {
    position: relative;
    bottom: 75px; /* 65, 115 normal*/
  }

  @keyframes LineFadeIn {
    0% {
      opacity: 0;
      d: path(
        "M 0 300 Q 0 300 0 300 Q 0 300 0 300 C 0 300 0 300 0 300 Q 0 300 0 300 "
      );
      stroke: #fff;
    }
    50% {
      opacity: 1;
      d: path(
        "M 0 300 Q 50 300 100 300 Q 250 300 350 300 C 350 300 500 300 650 300 Q 750 300 800 300"
      );
      stroke: #888bff;
    }
    100% {
      opacity: 1;
      d: path(
        "M -2 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 802 400"
      );
      stroke: #545581;
    }
  }
  @keyframes ContentFadeIn {
    0% {
      transform: translateY(-1rem);
      opacity: 0;
    }
    100% {
      transform: translateY(0);
      opacity: 1;
    }
  }
  @keyframes ImageFadeIn {
    0% {
      transform: translate(-0.5rem, -0.5rem) scale(1.05);
      opacity: 0;
      filter: blur(2px);
    }
    50% {
      opacity: 1;
      filter: blur(2px);
    }
    100% {
      transform: translateY(0) scale(1);
      opacity: 1;
      filter: blur(0);
    }
  }

  @media (min-width: 40rem) {
    .cards_item {
      width: 50%;
    }
  }

  @media (min-width: 56rem) {
    .cards_item {
      width: 33.3333%;
    }
  }
</style>


<div class="container">

  <li class="cards_item">
    <div class="card">
      <div class="card__image-container">
        <img class="card__image" src="https://images.unsplash.com/photo-1519999482648-25049ddd37b1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2126&q=80" alt="">
      </div>
        
        <svg class="card__svg" viewBox="0 0 800 500">

          <path d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400 L 800 500 L 0 500" stroke="transparent" fill="#333"/>
          <path class="card__line" d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400" stroke="pink" stroke-width="3" fill="transparent"/>
        </svg>
      
      <div class="card__content">
        <h1 class="card__title">E-commerce</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor praesentium at quod autem omnis.</p>
      </div>
    </div>
  </li>

    <li class="cards_item">
    <div class="card">
      <div class="card__image-container">
        <img class="card__image" src="https://images.unsplash.com/photo-1519999482648-25049ddd37b1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2126&q=80" alt="">
      </div>
        
        <svg class="card__svg" viewBox="0 0 800 500">

          <path d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400 L 800 500 L 0 500" stroke="transparent" fill="#333"/>
          <path class="card__line" d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400" stroke="pink" stroke-width="3" fill="transparent"/>
        </svg>
      
      <div class="card__content">
        <h1 class="card__title">E-commerce</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor praesentium at quod autem omnis.</p>
      </div>
    </div>
  </li>

  <li class="cards_item">
    <div class="card">
      <div class="card__image-container">
        <img class="card__image" src="https://images.unsplash.com/photo-1519999482648-25049ddd37b1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2126&q=80" alt="">
      </div>
        
        <svg class="card__svg" viewBox="0 0 800 500">

          <path d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400 L 800 500 L 0 500" stroke="transparent" fill="#333"/>
          <path class="card__line" d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650 300 Q 750 450 800 400" stroke="pink" stroke-width="3" fill="transparent"/>
        </svg>
      
      <div class="card__content">
        <h1 class="card__title">E-commerce</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor praesentium at quod autem omnis.</p>
      </div>
    </div>
  </li>


</div>