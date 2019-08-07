<script>
  import { onMount } from "svelte";

  onMount(() => {
    console.log("Functions are coming...");

    fetch("/.netlify/functions/hello")
      .then(response => response.json())
      .then(json => console.log(json));
  });
</script>
 
<style>
  section {
  }
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

  /* Button theme- rename */
  .theme-6 {
    --color-button-bg: #f7d337;
    --radius-button: 40px;
    padding-top: 20px;
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

  .glow-on-hover {
    width: 180px;
    height: 50px;
    border: none;
    outline: none;
    color: #ff3e00;
    background: #111;
    cursor: pointer;
    position: relative;
    z-index: 0;
    border-radius: 10px;
    font-weight: 600;
    font-size: 18px;
  }

  .glow-on-hover:before {
    content: "";
    background: linear-gradient(
      45deg,
      #ff0000,
      #ff7300,
      #fffb00,
      #48ff00,
      #00ffd5,
      #002bff,
      #7a00ff,
      #ff00c8,
      #ff0000
    );
    position: absolute;
    top: -2px;
    left: -2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
    border-radius: 10px;
  }

  .glow-on-hover:active {
    color: #000;
  }

  .glow-on-hover:active:after {
    background: transparent;
  }

  .glow-on-hover:hover:before {
    opacity: 1;
  }

  .glow-on-hover:after {
    z-index: -1;
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    background: #111;
    left: 0;
    top: 0;
    border-radius: 10px;
  }

  @keyframes glowing {
    0% {
      background-position: 0 0;
    }
    50% {
      background-position: 400% 0;
    }
    100% {
      background-position: 0 0;
    }
  }
</style>

<svelte:head>
  <title>Sapper netflify jamstack template</title>
</svelte:head>

<main class="page lanidng-page">
  <section class="portfolio-block block-intro">
    <div class="container">

     <div class="avatar" style="background-image: url(avatar.jpg)"></div>

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

          <a  href='about'>
          <button class="glow-on-hover" type="button">Portfolio</button>
          </a>
             

          </div>
        </div>
      </div>
    </div>
  </section>
</main>
