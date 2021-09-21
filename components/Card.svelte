<script>
</script>

<div class="card">
  <div class="circle"></div>
  <div class="content">
    <h2>Pepsi Cola</h2>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dicta expedita ullam modi odio dolorum unde dolor eum deleniti repellendus eius.</p>
    <a href="#">Buy Now</a>
  </div>
  <img src="./images/img.png" alt="">
</div>


<style>
  .card {
    position: relative;
    width: 600px;
    height: 350px;
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    transition: 0.5s;
  }
  .card .circle {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  .card .circle::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #d83133;
    clip-path: circle(120px at center);
    transition: 0.5s;
  }

  .card:hover .circle:before {
    background: #0065c3;
    clip-path: circle(400px at center);
    border-radius: 20px;
  }

  .card img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    height: 300px;
    pointer-events: none;
    transition: 0.5s;
  }

  .card:hover img {
    left: 72%;
    height: 500px;
  }

  .card .content {
    position: relative;
    width: 37%;
    left: 20%;
    padding: 0px 20px 20px 40px;
    transition: 0.5s;
    opacity: 0;
    visibility: hidden;
    text-align: justify;
  }

  .card:hover .content {
    left: 0;
    opacity: 1;
    visibility: visible;
  }

  .card .content h2 {
    color: #fff;
    text-transform: uppercase;
    font-size: 2em;
    line-height: 1em;
  }

  .card .content p {
    color: #fff;
  }

  .card .content a {
    position: relative;
    color: #111;
    padding: 10px 20px;
    border-radius: 10px;
    background: #fff;
    margin-top: 10px;
    display: inline-block;
    text-decoration: none;
    font-weight: 700;
  }

  @media (max-width: 991px) {
    .card {
      width: auto;
      max-width: 350px;
      align-items: flex-start;
    }

    .card:hover {
      height: 600px;
    }

    .card .content {
      width: 100%;
      left: 0;
      padding: 30px;
    }

    .card:hover img {
      top: 76%;
      left: 50%;
      height: 240px;
    }
  }
</style>