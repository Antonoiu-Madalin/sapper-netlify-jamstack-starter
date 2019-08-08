<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  i {
    opacity: 0;
    font-size: 18px;
    color: #fff;
    will-change: transform;
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    -webkit-transition: all 0.2s ease;
    transition: all 0.2s ease;
  }
  h2 {
    pointer-events: none;
  }

  .container {
    max-width: 500px;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin: auto;
  }
  .container .card {
    position: relative;
    width: 100%;
    height: 200px;
    background-color: #fff;
    overflow: hidden;
    margin-bottom: 4px;
  }

  .container .card:before {
    content: "";
    z-index: 99;
    position: absolute;
    top: -10px;
    left: 32px;
    display: block;
    width: 16px;
    height: 16px;
    border-radius: 16px;
    background-color: #e6e5e1;
  }
  .container .card:after {
    content: "";
    z-index: 99;
    position: absolute;
    bottom: -10px;
    left: 32px;
    display: block;
    width: 16px;
    height: 16px;
    border-radius: 16px;
    background-color: #e6e5e1;
  }
  .container .card ul {
    z-index: 99;
    position: absolute;
    left: 39px;
    top: 5px;
    list-style-type: none;
  }
  .container .card ul li {
    width: 2px;
    height: 2px;
    border-radius: 2px;
    margin: 6px 0;
    background-color: #e6e5e1;
  }
  .container .card h2 {
    z-index: 99;
    font-family: "Poppins", sans-serif;
    position: absolute;
    bottom: 0;
    right: 130px;
    font-size: 60px;
    font-weight: 700;
    color: #fff;
  }
  .container .card .fa-arrow-right {
    z-index: 100;
    position: absolute;
    right: 75px;
    bottom: 25px;
    font-size: 40px;
    cursor: pointer;
  }
  .container .card p {
    z-index: 99;
    position: absolute;
    top: 20px;
    right: 70px;
    color: #333;
    opacity: 0.7;
    font-size: 12px;
    letter-spacing: 1px;
    writing-mode: vertical-lr;
    -webkit-transition: all 0.2s ease;
    transition: all 0.2s ease;
  }
  .container .card .pic {
    z-index: 100;
    width: 80%;
    height: 200px;
    background-image: url("https://images.unsplash.com/photo-1525543907410-b2562b6796d6?ixlib=rb-0.3.5&s=9ff8e5e718a6a40cbd0e1471235912f4&auto=format&fit=crop&w=3452&q=80");
    background-size: 100% 100%;
    filter: grayscale(100%);
  }
  .container .card .social {
    position: absolute;
    left: 60px;
    margin: auto;
    top: 0;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-pack: distribute;
    justify-content: space-around;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    width: 180px;
    height: 64px;
    border-radius: 80px;
  }
  .container .card .social i:nth-of-type(1) {
    -webkit-transition-delay: 0.4s;
    transition-delay: 0.4s;
  }
  .container .card .social i:nth-of-type(2) {
    -webkit-transition-delay: 0.3s;
    transition-delay: 0.3s;
  }
  .container .card .social i:nth-of-type(3) {
    -webkit-transition-delay: 0.2s;
    transition-delay: 0.2s;
  }
  .container .card .social i:nth-of-type(4) {
    -webkit-transition-delay: 0.1s;
    transition-delay: 0.1s;
  }
  .container .card:hover i {
    opacity: 1;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  .container .card button {
    position: absolute;
    right: 14px;
    bottom: 14px;
    width: 30px;
    height: 30px;
    background-color: #da4d1d;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    outline: none;
    transition: all 0.3s ease;
    mix-blend-mode: hard-light;
  }

  .container .card:hover button {
    transform: scale(16.5);
  }
  .container .card:hover p {
    color: #fff;
  }
  .container .card:hover .pic {
    filter: grayscale(0);
  }
  .container .card2 .pic {
    background-image: url("https://images.unsplash.com/photo-1528785198459-ec50485704c7?ixlib=rb-0.3.5&s=3a2fc3039516555bbb2e9cd2967bd321&auto=format&fit=crop&w=1537&q=80");
  }
  .container .card2 button {
    background-color: #2b26c3;
  }

  @media (max-width: 580px) {
    .container .card p {
      right: 60px;
    }
    .container .card:hover button {
      transform: scale(13.5);
    }
    .container .card h2 {
      font-size: 40px;
      font-weight: 700;
      right: 110px;
    }
    .container .card .fa-arrow-right {
      right: 65px;
      bottom: 25px;
      font-size: 30px;
    }
  }
  @media (max-width: 530px) {
    .container .card p {
      right: 50px;
    }
    .container .card:hover button {
      transform: scale(12);
    }
  }

  @media (max-width: 490px) {
    .container .card p {
      right: 40px;
    }

    .container .card .social {
      left: 30px;
    }
  }

  @media (max-width: 470px) {
    .container .card {
      height: 150px;
    }
    .container .card:hover button {
      transform: scale(9.8);
    }

    .container .card .fa-arrow-right {
      right: 45px;
      bottom: 8px;
      font-size: 25px;
    }
    .container .card h2 {
      font-size: 30px;
      font-weight: 600;
      right: 90px;
    }
  }

  @media (max-width: 460px) {
    .container .card:hover button {
      transform: scale(8.5);
    }
    .container .card h2 {
      font-size: 30px;
      font-weight: 600;
      right: 80px;
    }
  }

  @media (max-width: 390px) {
    .container .card:hover button {
      transform: scale(11.5);
    }
    .container .card {
      height: 120px;
    }
    .container .card p {
      right: 20px;
    }
    .container .card .social {
      left: 40px;
      width: 120px;
    }
    .container .card button {
      right: 7px;
      bottom: 7px;
      width: 20px;
      height: 20px;
    }
    .container .card2 button {
      right: 7px;
      bottom: 7px;
      width: 20px;
      height: 20px;
    }

    .container .card .fa-arrow-right {
      right: 50px;
      bottom: 8px;
      font-size: 17px;
    }
    .container .card h2 {
      font-size: 25px;
      font-weight: 600;
      right: 70px;
    }
  }
</style>

<div class="container">
  <div class="card">
    <h2>Blog</h2>
    <i class="fas fa-arrow-right" />
    <p>a lonely trip.</p>
    <div class="pic" />
    <ul>
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
    </ul>
    <div class="social">
      <i class="fab fa-facebook-f" />
      <i class="fab fa-twitter" />
      <i class="fab fa-instagram" />
      <i class="fab fa-github" />
    </div>
    <button />
  </div>

  <div class="card card2">
    <h2>Vauxhall</h2>
    <i class="fas fa-arrow-right" />
    <p>a lonely trip.</p>
    <div class="pic" />
    <ul>
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
    </ul>
    <div class="social">
      <i class="fab fa-facebook-f" />
      <i class="fab fa-twitter" />
      <i class="fab fa-instagram" />
      <i class="fab fa-github" />
    </div>
    <button />
  </div>

  <div class="card">
    <h2>Blog</h2>
    <i class="fas fa-arrow-right" />
    <p>a lonely trip.</p>
    <div class="pic" />
    <ul>
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
    </ul>
    <div class="social">
      <i class="fab fa-facebook-f" />
      <i class="fab fa-twitter" />
      <i class="fab fa-instagram" />
      <i class="fab fa-github" />
    </div>
    <button />
  </div>
</div>
