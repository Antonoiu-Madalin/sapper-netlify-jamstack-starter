<style>
  /* To give card different colour filling, change .card background and card_svg path first option*/
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
    background: #b52e31;
    display: flex;
    border-radius: 6px;
    color: #aaa;
    box-shadow: 0 0.25rem 0.25rem rgba(0, 0, 0, 0.2), 0 0 1rem rgba(0, 0, 0, 0.2);
    overflow: hidden;
    flex-direction: column;
    opacity: 0;
    animation: LineFadeIn 0.2s 0.2s forwards ease-in;
  }
  .card__line {
    opacity: 0;
    animation: LineFadeIn 0.25s 0.25s forwards ease-in;
  }
  .card__image {
    opacity: 0;
    animation: ImageFadeIn 0.4s 0.6s forwards;
  }
  .card__content {
    opacity: 0;
    animation: ContentFadeIn 0.6s 0.8s forwards;
    padding: 0 10px;
    margin-top: -3rem;
  }
  .card__image-container {
    margin: auto;
  }
  .card__svg {
    position: relative;
    margin-top: -6.5rem;
  }
  .card__title {
    color: white;
    font-weight: 800;
    letter-spacing: 0.01em;
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
  @media (max-width: 341px) {
    .card__title {
      font-size: 140%;
    }
    .card__content {
      margin-top: -1rem;
    }
    .card__svg {
      position: relative;
      margin-top: -6rem;
    }
  }
  @media (min-width: 330px) and (max-width: 364px) {
    .card__content {
      margin-top: -1.5rem;
    }
    .card__svg {
      margin-top: -7rem;
    }
  }
  @media (min-width: 365px) and (max-width: 394px) {
    .card__svg {
      margin-top: -8rem;
    }
  }
  @media (min-width: 395px) and (max-width: 439px) {
    .card__svg {
      margin-top: -9.5rem;
    }
  }
  @media (min-width: 440px) and (max-width: 488px) {
    .card__svg {
      margin-top: -11rem;
    }
  }
  @media (min-width: 489px) and (max-width: 530px) {
    .card__svg {
      margin-top: -12.5rem;
    }
  }
  @media (min-width: 531px) and (max-width: 570px) {
    .card__svg {
      margin-top: -14rem;
    }
  }
  @media (min-width: 571px) and (max-width: 610px) {
    .card__svg {
      margin-top: -15.5rem;
    }
  }
  @media (min-width: 611px) and (max-width: 645px) {
    .card__svg {
      margin-top: -17rem;
    }
  }
  @media (min-width: 40rem) {
    .cards_item {
      width: 50%;
    }
    .card__svg {
      margin-top: -9rem;
    }
  }
  @media (min-width: 735px) and (max-width: 896px) {
    .card__svg {
      margin-top: -10.5rem;
    }
  }
  @media (min-width: 56rem) {
    .cards_item {
      width: 33.3333%;
    }
    .card__content {
      margin-top: -1.5rem;
    }
    .card__svg {
      margin-top: -7.5rem;
    }
  }
</style>

<div class="container">

  <li class="cards_item">
    <div class="card">
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
          fill="#b52e31" />
        <path
          class="card__line"
          d="M 0 100 Q 50 200 100 250 Q 250 400 350 300 C 400 250 550 150 650
          300 Q 750 450 800 400"
          stroke="pink"
          stroke-width="3"
          fill="transparent" />
      </svg>

      <div class="card__content">
        <h1 class="card__title">E-commerce</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta dolor
          praesentium at quod autem omnis.
        </p>
      </div>
    </div>
  </li>

  <li class="cards_item">
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
          fill="#b52e31" />
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

  <li class="cards_item">
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
          fill="#b52e31" />
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

  <li class="cards_item">
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
          fill="#b52e31" />
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

  <li class="cards_item">
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
          fill="#b52e31" />
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

  <li class="cards_item">
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
          fill="#b52e31" />
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
