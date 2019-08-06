<script>
  import { onMount } from "svelte";

  onMount(() => {
    console.log("Functions are coming...");

    fetch("/.netlify/functions/hello")
      .then(response => response.json())
      .then(json => console.log(json));
  });

  let avatAr =
    "https://raw.githubusercontent.com/Antonoiu-Madalin/my-portfolio-unclean/master/assets/img/37185104_2140359479532106_2518914451277611008_o.jpg?token=AE66ESTT6KWPG4TD7IH5VN25JHCY2"
</script>

<style>
  /* Portfolio important settings */
  .portfolio-block {
    padding-top: 100px;
    text-align: center;
    padding-left: 15px;
    padding-right: 15px;
  }

  /* Must be placed right after. Clears text on lower screens */
  @media (max-width: 576px) {
    .portfolio-block {
      padding-top: 50px;
    }

    .portfolio-block.block-intro .about-me {
      width: 320px;
    }
  }

  .portfolio-block.block-intro .about-me {
    max-width: 750px;
    margin: 0 auto;
    padding-top: 8px;
    padding-bottom: 0px;
  }

  .portfolio-block.block-intro p {
    font-size: 1.5em;
    font-weight: 300;
    margin-top: 20px;
  }

  .portfolio-block.block-intro .avatar {
    width: 150px;
    height: 150px;
    background-size: cover;
    background-repeat: no-repeat;
    margin: auto;
    border-radius: 100px;
    margin-bottom: 30px;
  }

  /* Background color*/

  /* H1 Boldness */
  strong {
    font-weight: bold;
  }
  /* particles.css *
    /* Position of the after-effect - above */
  .particles {
    position: relative;
    grid-area: 1 / 1 / 2 / 2;
  }
  /* Position of the after-effect - below */
  .particles-canvas {
    position: absolute;
    pointer-events: none;
    top: 50%;
    left: 50%;
    transform: translate3d(-50%, -50%, 0);
  }
  /* Position of the after-effect - left */
  .particles-wrapper {
    position: relative;
    display: inline-block;
    overflow: hidden;
    will-change: transform;
  }

  a {
    max-width: 200px;
  }

  /* Button theme- rename */
  .theme-6 {
    --color-button-bg: #f7d337;
    --radius-button: 40px;
    padding-top: 20px;
    outline: none;
  }
  /* Button height and cursor pointer*/
  button {
    line-height: normal;
    cursor: pointer;
  }

  /* The button itself */
  .particles-button {
    border-radius: var(--radius-button);
    background: var(--color-button-bg);
    border: 0;
    padding: 1.5rem 3rem;
    font-weight: 600;
    color: #11161f;
    font-family: Tahoma, Geneva, sans-serif;
    font-size: 15px;
    outline: none;
  }

  /* Hide anchor hightlight! */
  a {
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    -webkit-tap-highlight-color: transparent;
  }

  /* Remove hightlight on click */
  .particles-button:focus {
    outline: none;
  }

  /*Experimental avatar*/
  .avatar {
    height: 200px;
    position: relative;
    width: 200px;
  }
  .avatar img {
    border-radius: 9999px;
    height: 100%;
    position: relative;
    width: 100%;
    z-index: 2;
  }

  .grid__item {
    outline: none;
  }

  theme-6 {
    outline: none;
  }

  @keyframes cycle-colors {
    0% {
      border-color: hsl(0, 100%, 50%);
    }
    25% {
      border-color: hsl(90, 100%, 50%);
    }
    50% {
      border-color: hsl(180, 100%, 50%);
    }
    75% {
      border-color: hsl(270, 100%, 50%);
    }
    100% {
      border-color: hsl(360, 100%, 50%);
    }
  }
  @keyframes pulse {
    to {
      opacity: 0;
      transform: scale(1);
    }
  }
  .avatar::before,
  .avatar::after {
    animation: pulse 5s linear infinite;
    border: #fff solid 5px;
    border-radius: 99999px;
    box-sizing: border-box;
    content: " ";
    height: 140%;
    left: -20%;
    opacity: 0.6;
    position: absolute;
    top: -20%;
    transform: scale(0.714);
    width: 140%;
    z-index: 1;
  }
  .avatar::after {
    animation-delay: 2s;
  }

  /* Fixed anchor click only button and centered*/
  .anchorControl {
    width: 107px;
    text-align: center;
    display: table;
    margin: 0 auto;
  }
</style>

<svelte:head>
  <title>Sapper netflify jamstack template</title>
</svelte:head>
<main class="page lanidng-page">
  <section class="portfolio-block block-intro">
    <div class="container">
      <img src={avatAr} alt="Me dancing" class="avatar" />
      <div class="about-me">
        <p style="color: rgb(160,175,190);">
          Hello! I am&nbsp;
          <strong>Madalin Antonoiu</strong>
          . I work as a full stack web developer. I have a passion for creating
          blazing fast, pixel perfect, responsive &nbsp;websites.
          <br />
        </p>
        <div class="grid__item theme-6">
          <div class="anchorControl">
            <a href="javascript:delay('index4.html')">
              <button class="particles-button">Portfolio</button>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>
