<script>
  function onClick() {
    const audio = new Audio('pop.ogg');
    audio.play();
    const img = document.querySelector('.PopCat');
    img.src = 'opencat.png';
    setTimeout(() => {
      img.src = 'closecat.png';
    }, 100);
  }
</script>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <link rel="icon" href="/void_bg.png">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <meta name="theme-color" content="#000000">
    <meta name="description" content="Web site created using svelte">
    <link rel="apple-touch-icon" href="void_bg.png">
    <link rel="manifest" href="/manifest.json">
    <title>Pop Cat</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root">
      <div class="App">
        <div class="App">
          <h1 class="Title">탈선린!!</h1>
          <img class="PopCat" src="closecat.png" alt="GNU cat" height="100%" on:click={onClick}>
        </div>
      </div>
    </div>
  </body>
</html>

<style>
  body{
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    font-family:-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Oxygen,Ubuntu,Cantarell,Fira Sans,Droid Sans,Helvetica Neue,sans-serif;
    margin:0
}
body{
    align-items:center;
    background:#d3d3d3;
    display:flex;
    justify-content:center
}
.App{
    text-align:center
}
.PopCat{
    -webkit-touch-callout:none;
    -webkit-user-select:none;
    user-select:none
}
.Title{
    font-size:60px
}
@media (prefers-reduced-motion:no-preference){
    .Title{
        -webkit-animation:Title-spin 1.5s linear infinite;
        animation:Title-spin 1.5s linear infinite
    }
}
@-webkit-keyframes Title-spin{
    0%{
        -webkit-transform:rotate(0deg);
        transform:rotate(0deg)
    }
    to{
        -webkit-transform:rotate(1turn);
        transform:rotate(1turn)
    }
}
@keyframes Title-spin{
    0%{
        -webkit-transform:rotate(0deg);
        transform:rotate(0deg)
    }
    to{
        -webkit-transform:rotate(1turn);
        transform:rotate(1turn)
    }
}
</style>
